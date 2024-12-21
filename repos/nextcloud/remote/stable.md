## `nextcloud:stable`

```console
$ docker pull nextcloud@sha256:b9e447b0c8f71fd1442309d63576a1f0696cea3ead06a7a7ad9f303bdcdab000
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

### `nextcloud:stable` - linux; amd64

```console
$ docker pull nextcloud@sha256:397e37af5b9bce56e4ea771ea28dfa71cb0f735b76d5972ed790425b3bff48bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.2 MB (425241417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b93832d34356c65fa527ae76daf1562ed646b2b6bc89e9121c2af362f0ff48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a964551c533750a79844cd9ea6afc02321399087330588960acb396b1b163f`  
		Last Modified: Fri, 20 Dec 2024 21:35:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc1f8732563b856747fa5497fbde1f3cddadc07307f59a3931c5b35ffc61cce`  
		Last Modified: Fri, 20 Dec 2024 21:35:10 GMT  
		Size: 104.2 MB (104150565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb55caf86bf6fe3d0a3ea2c414066c2887de3c1df1f5cc53152943290bf5a58`  
		Last Modified: Fri, 20 Dec 2024 21:35:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b887f8fd83934add05de1dd84d889066d0710768bcd74ae4756f34b675fea5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:08 GMT  
		Size: 20.1 MB (20123809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0860560e09adf9edb7e4434662457d4877a84e1433d4c9fd22f5d0214bb916`  
		Last Modified: Fri, 20 Dec 2024 21:35:09 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f17bce6d22ffa8c4d56a65465e7fe6228548108735a2fb69772a0b9ac06d4d`  
		Last Modified: Fri, 20 Dec 2024 21:35:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4086ca69645da2a45c63ef4aa2cf0745f6ea543e150df4e39beef7751b644017`  
		Last Modified: Fri, 20 Dec 2024 21:35:10 GMT  
		Size: 12.3 MB (12279815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483ebb8015e48376c76e9fb322ba94c8fb8756b64e09c2313bfcfb20410b649`  
		Last Modified: Fri, 20 Dec 2024 21:35:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e27c3033e722a50d5882b771b2462b8797e398128d990ee3e01ba3c30dfed0`  
		Last Modified: Fri, 20 Dec 2024 21:35:10 GMT  
		Size: 11.4 MB (11419178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d231d33f814dc59f618233b8dcb323c7dbec7516eff470f72aac76f8acbb33`  
		Last Modified: Fri, 20 Dec 2024 21:35:10 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48816137dddb860de9b36c19a1fc0016e83e55c3b785bb2c8b2d9f3e43c44149`  
		Last Modified: Fri, 20 Dec 2024 21:35:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462124a62e7e11c667ea50481b73a9718930f0600d84e6209c3fc84b9e834193`  
		Last Modified: Fri, 20 Dec 2024 21:35:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5120ecb0178d959dca6bfead284fa58be8df9f216fdd95c9028fb6c1d146b6a`  
		Last Modified: Fri, 20 Dec 2024 22:35:14 GMT  
		Size: 22.8 MB (22784265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff407cf977595055a9a8f4dd23e5323cf995b8a16229feedee5165e62ab0c22`  
		Last Modified: Fri, 20 Dec 2024 22:35:13 GMT  
		Size: 20.7 MB (20739898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3f63e3c2ef5d8a3dc2b9531371ffceb3350a2b1ec16581671bf9b372196dc`  
		Last Modified: Fri, 20 Dec 2024 22:35:12 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626fee306f22da05837d47fbe85320dbf8e29dae792af82d10e57f3ccb0b58e`  
		Last Modified: Fri, 20 Dec 2024 22:35:13 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a08d5b9fc13f76cd539e86e215ee8f1d412e2bbd9124914a6d36c4ee49b16f`  
		Last Modified: Fri, 20 Dec 2024 22:35:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54d0602983822622bfbee3d0ecaa9a5a4154562d1ead2fe1572fdf493509d58`  
		Last Modified: Fri, 20 Dec 2024 22:35:19 GMT  
		Size: 205.5 MB (205498865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573a841713c165135122d445f80c98165d1643ce4e5747a74ee17562e6ea227`  
		Last Modified: Fri, 20 Dec 2024 22:35:14 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81a9801607c29605fdaf53920fd0abdcbc83cd06c251190f6ce6e67c55f4766`  
		Last Modified: Fri, 20 Dec 2024 22:35:15 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:86b957844ef7bf829c7e52a1aa313dcdb11753676a1bc215e195c562598777e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 KB (60976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a3c024b6364d49e19eae87232125c1db778f512fabc6313830c68987528db9`

```dockerfile
```

-	Layers:
	-	`sha256:f939e6b5d0b73400b57b8e1af32a45eeab388063dd62e09bee7a67e9142d137f`  
		Last Modified: Fri, 20 Dec 2024 22:35:12 GMT  
		Size: 61.0 KB (60976 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:65d2b993fd2a169b790ede7525f5c76f5dbda52ef47b6979628254e29500454b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.5 MB (394496382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca59bd5e1ddbad7b666e8248985dd8cbc3cf5573705a0fc557a29cfecf351641`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f38f689bfc81a80b77922476ec5fa4c66c3c95c18a88e0d5c163e4f88a3fa2`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391778530ecd6fb67099da1af9389d8c5e85a5bf4eda9154dc075982c5d03aa`  
		Last Modified: Tue, 03 Dec 2024 02:47:27 GMT  
		Size: 81.8 MB (81799353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730374a8da7a42b29a8cb7308121c86932f17cf03f72bcbc1157654eab662c6`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d43114e6dacb9dea8dc21a7254e5e88b1cc12a6d007a1431166907121528d6`  
		Last Modified: Tue, 03 Dec 2024 02:51:31 GMT  
		Size: 19.4 MB (19418860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fab695d67cbdff447c2ab807f8900e1d2a4dce642475708bed149bbdd54dab`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e205d192900e0b63fd0542c47e1a455fa0a703afa9932fd48ab46e05557439`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06988a411a9d9775775ab4f27e46d8c92a31d76467fe0b0972dc2367770ee3c9`  
		Last Modified: Fri, 20 Dec 2024 22:27:11 GMT  
		Size: 12.3 MB (12277725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19384cb6dee65b7727f1e62ec3ff6d4705e81027b08efb9a5709fd00de28338`  
		Last Modified: Fri, 20 Dec 2024 22:27:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39f409d2e7b37981b30fbd547c85fa4eebb1b39942e4f5ea069571bc6b04db4`  
		Last Modified: Fri, 20 Dec 2024 22:27:11 GMT  
		Size: 10.4 MB (10404317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983731a59f9893d3126ed077b7681ecddb457773fd7fe07dc691d56527f50e3c`  
		Last Modified: Fri, 20 Dec 2024 22:27:10 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3679fa7763bfd07df089a61b6fc7b82fb13bb894fffc8676f641fd55e4bcec`  
		Last Modified: Fri, 20 Dec 2024 22:27:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb49f8862be2812d7e5eeb571104ba3f0adf4f207f15c60cd62f02faa74b61f`  
		Last Modified: Fri, 20 Dec 2024 22:27:11 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9476faa78dfcd06df0693ac028870689241f31dadbaff8d22c3fe62a6f6437c9`  
		Last Modified: Fri, 20 Dec 2024 23:49:35 GMT  
		Size: 19.9 MB (19896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c60bdf97a822257a5c90cb21dee9c6b9a28b11c7236650cbc8519ce0564c2a7`  
		Last Modified: Fri, 20 Dec 2024 23:49:35 GMT  
		Size: 19.4 MB (19434388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c259abf56d1d93725808fda47d56213db5d33b5ff5d78ffbb9afeb3ac9fdec3b`  
		Last Modified: Fri, 20 Dec 2024 23:49:34 GMT  
		Size: 719.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61078c63e23257fe8f411e0b325717dae441401bd17dc26ee850826d2dd99890`  
		Last Modified: Fri, 20 Dec 2024 23:49:34 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d75921a7e8d7cac25064107b0396b4863df18b5587c46f326c4260e00514cb`  
		Last Modified: Fri, 20 Dec 2024 23:49:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d5b2b4a767e70a6703f74b8f42f9afd916d035061a999f25159aa97b2577c`  
		Last Modified: Sat, 21 Dec 2024 00:00:21 GMT  
		Size: 205.5 MB (205497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294dbfa78eb6eaf4a8c0481504bf69f9e08f517cb22ad1dc377fcf4a084e6c8e`  
		Last Modified: Sat, 21 Dec 2024 00:00:16 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a69082a21bb5f26d59cae1b78cc1db5dfcde343b44007d675b31985872f046`  
		Last Modified: Sat, 21 Dec 2024 00:00:16 GMT  
		Size: 2.4 KB (2399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:e800c1be226cde38b38b168be833d6bd1e3e519da81cc5761acbe485b2a0db63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250074309648d8bd6cd94a4a318714539757ba5bc1b5105acec4185dd0dbcf2a`

```dockerfile
```

-	Layers:
	-	`sha256:0847dc7a082fc54771cf4c6e6f223ce8f922acd90465b4f7d25bea864f19dc62`  
		Last Modified: Sat, 21 Dec 2024 00:00:15 GMT  
		Size: 61.2 KB (61172 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:e9e5f71ea9a0092a94b36789ec905a401d49422a89c78731d1b4effb908ad789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383270534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456a7ee8befe323e1da7a205492447082e166eeb667c24bdfec2f5a204aeebc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc399a814abef0b215a25083103b4fcd6382c3040364b6565271bfaad3edcda`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c111bef206c9990ed304a2c9e0dbc3e87552d4023cb73e5796908ce98c5a16`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 76.0 MB (75969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c345ebeb8ac614dcc4ff559e2cf2d693ff887d5cb958080625dc4d803abd018`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64247e8882ecb48484c43614c1bd400c9f3fa7ff601a3e74f81606279623eca2`  
		Last Modified: Tue, 03 Dec 2024 02:49:32 GMT  
		Size: 18.9 MB (18857266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489174183fa221f132d5b3d11e3bf9b32527d04508f03839c9a1555913aeb51b`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5de890f1f55562915effb16f54430acf049d0013e862b5942f473118fe5ed`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b569e4be24abc5ba63a94af7030efb9e2fcc0d7d1973a825db389056216a7454`  
		Last Modified: Fri, 20 Dec 2024 23:37:22 GMT  
		Size: 12.3 MB (12277662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7a0f65b537ae02aeb76b9567c5423b0ed73dfcd2a4105de0f53b1ffad91a3f`  
		Last Modified: Fri, 20 Dec 2024 23:37:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0b7bcde19d7f1d22f633da37dd6cbab9bb0b6761f4a063308f252ac76c9600`  
		Last Modified: Fri, 20 Dec 2024 23:37:22 GMT  
		Size: 9.8 MB (9833561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509ef79d972d85182471f51370c0bcc3b120eec04ec706975eb98e2a80e1f105`  
		Last Modified: Fri, 20 Dec 2024 23:37:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8d0cdced75cdb302e711db50134ee13559e3f31b40489e0730fa29b249601e`  
		Last Modified: Fri, 20 Dec 2024 23:37:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ffb90be17cb3ab30dff5cce8ce1497f1dfa47fa942441e609e8dbb8f022dca`  
		Last Modified: Fri, 20 Dec 2024 23:37:23 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a033ff3e8e9e422cf6d4839d75e49067a2ffcd359239cf2407e32b7025f0476a`  
		Last Modified: Sat, 21 Dec 2024 02:01:42 GMT  
		Size: 18.1 MB (18135739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c176d5fa195ca1611d27d64cebeea7607875c379b39e75f52e1a9ccfb1e2fd`  
		Last Modified: Sat, 21 Dec 2024 02:01:42 GMT  
		Size: 18.8 MB (18753223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bc6908a1814a8b13161e623a239068731e18a52fa49883ca0b94e50bac9c42`  
		Last Modified: Sat, 21 Dec 2024 02:01:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165d7e142337306a1d8d5b818d4c1719d6666294b957d709762a39b70d3444bd`  
		Last Modified: Sat, 21 Dec 2024 02:01:42 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441954c118ab2cdf05e31436b8625318b53c94520cc22021933e8001aa9a0f34`  
		Last Modified: Sat, 21 Dec 2024 02:01:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30e8e025fc4c57a5be0c965cfdd1fc38cb2a8e4b26275c8892c83d06cfe0bd2`  
		Last Modified: Sat, 21 Dec 2024 02:11:58 GMT  
		Size: 205.5 MB (205496840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1a0156389001f8dbcb7da829bf8f40fac51d173ee3da75870b923150d27e1b`  
		Last Modified: Sat, 21 Dec 2024 02:11:53 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd015b039e699de5d5bad141e17abfc7b58d83d77fd752a2d245b4005876f3`  
		Last Modified: Sat, 21 Dec 2024 02:11:53 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7f136b95293a20f1243098ada1dbaf3b4396162b843db5cfd28ade84f26591dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3c75f80475ebfc7559ec350789566b71bce8a2589754d330d151ba32a3824`

```dockerfile
```

-	Layers:
	-	`sha256:7b0ea241dd348da65701629f4b9ac1c36412d7b275168d4fe569f767ce1ec16c`  
		Last Modified: Sat, 21 Dec 2024 02:11:52 GMT  
		Size: 61.2 KB (61162 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:b38c88ef3d90e76a24d67d47870aba6cb67367eaf70a5801ce9bb80889ed5091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.4 MB (416432222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b786bfd20d4de1af42a003093502e63d56f1777889f8d4561709e51df766eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 04:48:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 04:48:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 04:48:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_VERSION=8.2.26
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 04:48:20 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 04:48:20 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 04:48:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 04:48:20 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b3b5e04c8b4e6110fb0e212055b9c7eb2aaa1cf8779fd681a2462f67111a8`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc980920c054a940b9793a107341acd51b059aed873177ef237579d941f23ef`  
		Last Modified: Tue, 03 Dec 2024 03:01:11 GMT  
		Size: 97.9 MB (97936346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130ec09764042703bb02f30348dab7ba0380d619963d04ab8ccc9678ca27470`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487dfea6acc671d5a73050d1cb6d9894d55ab6f79fe82e0916fd83c0ee4c37`  
		Last Modified: Tue, 03 Dec 2024 03:04:46 GMT  
		Size: 20.1 MB (20120928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970f3d36c66c0d81d84d5b43bd8a643ca7669c83b51b9efe950944e0ae9d6b4`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe821f4633e8a7a268f1b2ee321ff810e3810688d047ab340d79ad5a71f116`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f5d857df6cd896fca1ec20962f8507e55f1f434f0782115f25018472881524`  
		Last Modified: Tue, 03 Dec 2024 04:01:54 GMT  
		Size: 12.3 MB (12267326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f7bb88ea9faa7fb71a284556199533e86a11b6ea608cdca24527b2fb50fc9`  
		Last Modified: Tue, 03 Dec 2024 04:01:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52087d0e8882e6a2195fe0bd89d6d2cb7f19138889f246aa9ec5d2ec63fd357f`  
		Last Modified: Tue, 03 Dec 2024 04:01:54 GMT  
		Size: 11.4 MB (11423468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b790ab7de78e837229f4cc66541e454a4a87e83c34047c3c8f71c43ccee480e9`  
		Last Modified: Tue, 03 Dec 2024 04:01:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36982426b87e6afa20109ad4c85959be1687e12b313d497a4eaff3c1db6a5ee2`  
		Last Modified: Tue, 03 Dec 2024 04:01:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1d11241f99b0d945a56867d0320e7128a81da4627fc97b8b6794a938e6e06`  
		Last Modified: Tue, 03 Dec 2024 04:01:54 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae76a695a7687c670d81dd179a5ff0298bf4c2f4a59e7d6abab17a9fdf49d5c`  
		Last Modified: Thu, 12 Dec 2024 22:44:00 GMT  
		Size: 20.1 MB (20146692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41427378ec17c38e5701f277fcf6557e0a5fd6e529c40cd40de8c25bec610c8d`  
		Last Modified: Thu, 12 Dec 2024 22:44:00 GMT  
		Size: 21.0 MB (20966293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8405911d36f419f50cbda7552c0866a1aed22857a29f27c8b2e168ad2b00c2`  
		Last Modified: Thu, 12 Dec 2024 22:43:59 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81ea2c91c5a974b11d69064aa947aa75b606a2c1bf5d13e1b2b9b3449a37ffe`  
		Last Modified: Thu, 12 Dec 2024 22:43:59 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05ef74403a629dd45fb2c9caf78d3dbd9417918130e9fc7107d0644b9aff1ec`  
		Last Modified: Thu, 12 Dec 2024 22:44:00 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7772ba4ab52077fc70bab525be9ba4e5f934548078bbadfca8d3d15947ef3f15`  
		Last Modified: Thu, 12 Dec 2024 22:54:54 GMT  
		Size: 205.5 MB (205498910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d384c5c7982ecc2e360a7886d7bfcb476cbd8339241aed1c0f46e4bc649c7b`  
		Last Modified: Thu, 12 Dec 2024 22:54:49 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fac52098d22ea3201776023afcd686225943a0e9524fc584b5b8dcd50812f5`  
		Last Modified: Thu, 12 Dec 2024 22:54:49 GMT  
		Size: 2.4 KB (2398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:36f1a8a5a533070dd60549f5dc7355e9cf9e95efc605e05085d5c74dff454e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23768145f6fe9ea2815ad6ff62118d7851156e7eb243f15a32606b6c1c5cac99`

```dockerfile
```

-	Layers:
	-	`sha256:bec5236712884461682519944c2a3b44c8f1b9b53792a37cfae8f49f7f33579b`  
		Last Modified: Thu, 12 Dec 2024 22:54:49 GMT  
		Size: 61.2 KB (61242 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; 386

```console
$ docker pull nextcloud@sha256:dcaed4255c860af19342bfc786f352e25cd7718f2eeece2e6697b3d279aeb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.8 MB (423816241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cc1f92f035aec9df8d6f8aa1ddd6102d407f5299719e235e2b0fc036b29046`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6097c0834e20b776aa0c8fb16adbc7077be4f9500178c2f1a847cc95b83549`  
		Last Modified: Fri, 20 Dec 2024 21:39:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f3fadd1ef0320a099dfb1d605b59a5a13557493f07ad02cc057739494e0397`  
		Last Modified: Fri, 20 Dec 2024 21:39:58 GMT  
		Size: 101.3 MB (101320546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a799f4291c3ff1f071ad444e73615f7cc773384a1be5b3ab8624818f3b20c8`  
		Last Modified: Fri, 20 Dec 2024 21:39:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1424f1b9cb4dc9f0388b3b48d438bf3ec06081fdc24941d2d07f5b1bda602f`  
		Last Modified: Fri, 20 Dec 2024 21:39:56 GMT  
		Size: 20.6 MB (20638469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5b10ff1206318600fa1e0d54919ab7b1b5b33782b9b9b2a23bdbcf8fc2b6bb`  
		Last Modified: Fri, 20 Dec 2024 21:39:56 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38657becd1bcf4e508591e855d488e866e88300c535323fe4c1430c9fa19e6`  
		Last Modified: Fri, 20 Dec 2024 21:39:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6868b8138e4bd9337724a81797e9add6717bb4247664589f7e821cda0f0bf5`  
		Last Modified: Fri, 20 Dec 2024 21:39:57 GMT  
		Size: 12.3 MB (12278781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf31979f269692d9d1cb6b318d3516a7a09e9ee9c6f7937620d6dc29715b10d5`  
		Last Modified: Fri, 20 Dec 2024 21:39:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a309c9561a6e1bb084a7f1ef4e7d0f30bd82b6514eec0836169527811ee0a6`  
		Last Modified: Fri, 20 Dec 2024 21:39:58 GMT  
		Size: 11.6 MB (11646896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45286ca7e8f1c1f7343faed2de9f0f85cb2d231bcafb32db61f29bb353bb681`  
		Last Modified: Fri, 20 Dec 2024 21:39:58 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c9c564a402dd66a4cab610875b2d11bba3f1016c57d3c352362432931cff3`  
		Last Modified: Fri, 20 Dec 2024 21:39:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9be021ca2d5be2e6b65ea718c57a9739504826f7bca53c3537cfd9af749008`  
		Last Modified: Fri, 20 Dec 2024 21:39:59 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e11c171cb3989fb6e0b0870d8221809d737c14c5917427e23ddbef517b7a21`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 22.3 MB (22261841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf8b2724c509dc074d268b08f65ae671a10b414b66abd3ca7ac97c118564781`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 21.0 MB (20953008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd19acace2a05dfc0b9468c713403f1cd47afdea97f0903dafe087005d98acf2`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5cc88aa1d6d67a003d8a86fdea17e412728b74764b7ad68ad6594774095fa3`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6c67c8d4d52962d1fc00d70d1b951dd32f1a7e640286b6f20635bcfd74573`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f92d647ebfc6ff32dafda9f3d9191d10abcee933906da85cf207ebe358f9716`  
		Last Modified: Fri, 20 Dec 2024 22:37:54 GMT  
		Size: 205.5 MB (205497770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976ae0a4b5b606f1379e067faf342d47bae64f9c7063527c3fc3e32966ebfe4`  
		Last Modified: Fri, 20 Dec 2024 22:37:50 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc31bcd176b26709b5c52a9221eca71ac5bf45dd4801767b13da65cfb1470b3`  
		Last Modified: Fri, 20 Dec 2024 22:37:50 GMT  
		Size: 2.4 KB (2398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3a32169856bd889419375f0f5e0c0f3b7f9161ffcdc0c676bd7ad5d6a353b9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 KB (60894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff40a86e197ac056161856ec943ebbbbd921cdb49a423e8fe480a83048d0cea9`

```dockerfile
```

-	Layers:
	-	`sha256:d8eaa394b11a1a3dcc326e91557f071e73f3860212deab1502923c95bd3ca436`  
		Last Modified: Fri, 20 Dec 2024 22:37:49 GMT  
		Size: 60.9 KB (60894 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; mips64le

```console
$ docker pull nextcloud@sha256:fe2af3c4566c1c9d83418c20b6e62bd0b986b64200a137d61cb07cc72ad266a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397637067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1df0aa51c43dc4dff122b5f6725c5113672c7766a6122dffb4cce9f3b26226`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 04:48:20 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 04:48:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 04:48:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_VERSION=8.2.26
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 04:48:20 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 04:48:20 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 04:48:20 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 04:48:20 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b6f869e689f1f7935effcea7aef7505ad04025b0311ff3937b9103eef46fd`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7f48524d255d2a114c61e2dea94f3576d2144432398eb626ed6bbb8da968d`  
		Last Modified: Tue, 03 Dec 2024 04:22:41 GMT  
		Size: 80.5 MB (80475126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c3c34315ea9a93e65cc52bfdaf45d8f691045833035294baddeaa21df2439`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df91c5aff622eeb49d30bc53aeda928e25ca30d9809e0caf1fc0dbcf6aec00dd`  
		Last Modified: Tue, 03 Dec 2024 04:42:14 GMT  
		Size: 20.1 MB (20069109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1873dc58b3bfe6549f8fd226713fa111f41803622dcaa71518533d1ab7f287`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa97de501943d58384491dc09430289a7e70957ada9f084524d32187e90f64`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ccbc4f179d8afc05abe53a20868f4412f49de95ea8f439d0f9580fbbcfa95`  
		Last Modified: Tue, 03 Dec 2024 07:01:01 GMT  
		Size: 12.3 MB (12265309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a6b1d3cdd3015974300a533cd7290b9bcad9ccbfec3b638f03d886f24db069`  
		Last Modified: Tue, 03 Dec 2024 07:00:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641bb0a36b8c5281f2785d784302f4772d214c52fae289909235179c17abe028`  
		Last Modified: Tue, 03 Dec 2024 07:01:03 GMT  
		Size: 10.5 MB (10494880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c0109bd3145c69091d9ff8c0335ea4ee50c8335887e8b61ddc1b3c6b1d21f`  
		Last Modified: Tue, 03 Dec 2024 07:00:59 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1b9476c2a0b9c371aa5f275536fee07444dc9537ac5e378340735151ca2d5a`  
		Last Modified: Tue, 03 Dec 2024 07:01:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7f3fbeff3ac06665d0513630644a9b517550a157e06f8754180e212355f417`  
		Last Modified: Tue, 03 Dec 2024 07:01:00 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eec0696bab8fa6569d711a2f8404477456dc4b4d16a409e60c6e005704ca8b8`  
		Last Modified: Wed, 04 Dec 2024 03:19:28 GMT  
		Size: 19.8 MB (19803061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb80ef650b3e59f846823dfb5ad6becce1e0eb9e8819189a509a32f5cc97968`  
		Last Modified: Wed, 04 Dec 2024 03:19:25 GMT  
		Size: 20.5 MB (20511792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9c70dc407a00ecfdf43fea85a60ecf52b3c2a3e15ae4df96e874bbb8de2b02`  
		Last Modified: Wed, 04 Dec 2024 03:19:22 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5012eb97ac8261dd350cf434d183bc0b9e80c3b7a6328201c86add8eeaaf276`  
		Last Modified: Wed, 04 Dec 2024 03:19:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fa8b50495751630fa5aa796d954e64d628f899264830286c5592600c434d8`  
		Last Modified: Wed, 04 Dec 2024 03:19:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47734fa7ef2b65f12ec3c9caacb2c5950d394a8b760f5fcea4b7b3f15364e6cd`  
		Last Modified: Thu, 12 Dec 2024 22:58:56 GMT  
		Size: 205.5 MB (205498428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910638c5a6113aa2ddaa718a05cb422857dfb44e9ebdcbfff16beeba7bd3af19`  
		Last Modified: Thu, 12 Dec 2024 22:58:37 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aead98583ec17393e9bdea27adb0bc482b72e85f4b3f74366ee3a487ef7bdce4`  
		Last Modified: Thu, 12 Dec 2024 22:58:38 GMT  
		Size: 2.4 KB (2397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3b881463ff894a3e458d34e9dce2f8c5589673a2ea3d821588d6f7a9183e649e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 KB (61120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2770857b598bd37bec648455486cc96990e7da907c4058d43b3d1bf1befc0158`

```dockerfile
```

-	Layers:
	-	`sha256:38c45ac4ac13964833580e5b9f5a67c482723aef7decba4aec020c212342704e`  
		Last Modified: Thu, 12 Dec 2024 22:58:37 GMT  
		Size: 61.1 KB (61120 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:f173082037c00cd35936a8a21baab00ebfd32d57dee2fc5a1df5823b691db9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.4 MB (430405703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ecdfacef586bbca2bf73746d175f9fa9e8d634ebded806596254f9c3e5971a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd0832c6742842354605a68e1c37e01805dbd8dcb42bed521f3b5ffc9d6782`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8241edc102752205916990cef5c543934549ef471e4363e3f37b4d609359e`  
		Last Modified: Tue, 03 Dec 2024 03:01:42 GMT  
		Size: 103.1 MB (103128469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe6a6422bc6eb2d0ecc0d78cfc1ccb6571b1ef03bf7b17f2384e77abef0c849`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be563cd21515e56438eeee24e165c5e6eb1efe06f45df830dbb193247c929683`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 21.3 MB (21308386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34863b54186af36b092695264d86f35c3119978d70427455e85f6fd279681048`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7b95b58340fb918a89b18f660a1045c0f902984f4cae1590b337184e865c1a`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f4266a31dc901870476587852334fb48100cd845471a28b47370955920c0b9`  
		Last Modified: Fri, 20 Dec 2024 22:50:23 GMT  
		Size: 12.3 MB (12279212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c719f6678a9f446fbd8a86f1926a89787952837326b45df502be7a1da7ff58`  
		Last Modified: Fri, 20 Dec 2024 22:50:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a89d1453610500e5501d6d968a0d093a9e095aea49082cc3e7b9b1cb864cc6`  
		Last Modified: Fri, 20 Dec 2024 22:50:23 GMT  
		Size: 11.8 MB (11833288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5ad57b25b0c69f3406f2254bce7b860bd388d9a28f9d31417380b2f2442935`  
		Last Modified: Fri, 20 Dec 2024 22:50:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03603519e9ce786adc30a58e62bf0c87ddc6ccf232aaeb41e7373f7c43fe4ed`  
		Last Modified: Fri, 20 Dec 2024 22:50:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca070906ef9b0f514ae34a0d7057d5d77c023691983e1def5990fad6972a23`  
		Last Modified: Fri, 20 Dec 2024 22:50:23 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1642c0029f3f9b4afbf724d647cccfa7460aa5058cc7c0fbf353aded4f69d`  
		Last Modified: Sat, 21 Dec 2024 02:38:02 GMT  
		Size: 22.6 MB (22623567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b6befc31b2a6b8e272c00c8f0efd13e1ae0827ae324222d1a1252c2cccdc7`  
		Last Modified: Sat, 21 Dec 2024 02:38:02 GMT  
		Size: 21.7 MB (21657119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b10007aee3b70a150132643f5b9418131c245568b5cb4901512496941187c29`  
		Last Modified: Sat, 21 Dec 2024 02:38:01 GMT  
		Size: 715.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e303e4c1228744dff3d1ab7e9a5e99f4935f77edbb31f6bc2496c4a238e0f6`  
		Last Modified: Sat, 21 Dec 2024 02:38:01 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0ba083e45c48cd3c87ab580e85ae6dad1db7425a82d9a6eee29bc3fca8813`  
		Last Modified: Sat, 21 Dec 2024 02:38:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8478af78c732e4f32d971b34b7f4d887796123ea9c0c8982892ace0387c807ff`  
		Last Modified: Sat, 21 Dec 2024 02:38:07 GMT  
		Size: 205.5 MB (205498931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a7715dd150748229dcfba8c0ccc71fdffabefb5b28c9bc10906aeb96abea55`  
		Last Modified: Sat, 21 Dec 2024 02:38:03 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c3c4d228f11294f1bc25043e720d65e6566286c4672402423ca994d9027fb`  
		Last Modified: Sat, 21 Dec 2024 02:38:03 GMT  
		Size: 2.4 KB (2398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:07a7afa4a1d3b3f479fe4d92e05514902b3219365ce0d8ab586534cd6de54e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 KB (61078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282973418b2844c24f5e7b605dd9de2eb0e160f307ef6c5ef5f62e29fe5dd8dd`

```dockerfile
```

-	Layers:
	-	`sha256:1a3e3552d7d9ae0b89d4319e67fbdba4f1b0765c528240895f1c050b2a602685`  
		Last Modified: Sat, 21 Dec 2024 02:38:00 GMT  
		Size: 61.1 KB (61078 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; s390x

```console
$ docker pull nextcloud@sha256:d2fbed4cdb0cd0afe653dfd1102d198a66e7d4e0b7b6f450b1fa84435364beb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395075791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fba4c12a601199f9fcc086a7dab9ed0767f222691bbb15522e5eb42c1aa2559`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 12:01:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_VERSION=8.2.27
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 12:01:29 GMT
STOPSIGNAL SIGWINCH
# Thu, 12 Dec 2024 12:01:29 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
WORKDIR /var/www/html
# Thu, 12 Dec 2024 12:01:29 GMT
EXPOSE map[80/tcp:{}]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
VOLUME [/var/www/html]
# Thu, 12 Dec 2024 12:01:29 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 12 Dec 2024 12:01:29 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENV NEXTCLOUD_VERSION=30.0.4
# Thu, 12 Dec 2024 12:01:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 12 Dec 2024 12:01:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Dec 2024 12:01:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6d88ca75be60fd842318e38796161d90dc699ddefddb72e584661cafccbb5`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1972b1cde205ce78e000379a6f103cc814e05cf048628db71370f4268b574`  
		Last Modified: Tue, 03 Dec 2024 02:45:10 GMT  
		Size: 80.6 MB (80624347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0df81e218837c9a0821f00169675df65b6dc92a07a5e60fb03eb1b30c73673`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81785c5e81e41257e9343844a3bb03f7c6b683f55e2dd07969f24adcc528917d`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 19.9 MB (19895239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b912aab84041841b2de0edb1264346e4f5aa519009fc0ab560ea1b76d041e127`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddea8579f46dc94efa149af85f249d1131297e7dcfce941798a62873eb5745`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6d3dac3c7ba97b537360130394ccbe8f23a69dc8bc36b682e146192bdc565c`  
		Last Modified: Fri, 20 Dec 2024 23:00:46 GMT  
		Size: 12.3 MB (12278090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0231ad811b3091ecd3cd3bb1d025f3f1d2bac5478f7dc2b5223bfbe185c823`  
		Last Modified: Fri, 20 Dec 2024 23:00:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f438e30ab1b033b12f6d7ad58081fb13f80b6bf7d5a66e2553bf3d8c2e3a9`  
		Last Modified: Fri, 20 Dec 2024 23:00:46 GMT  
		Size: 10.7 MB (10650053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fff6e5c5479fcdca6ea79459ad7ca49143028a740e50da65d536b17680abc9`  
		Last Modified: Fri, 20 Dec 2024 23:00:45 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4414464f567eb5bbc9d8228380ec921d7aadd457f135458af1af07c685e1cf`  
		Last Modified: Fri, 20 Dec 2024 23:00:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46187d9f0fa3394692c436742855406114dd3d532639d00b8124f889980e3b2f`  
		Last Modified: Fri, 20 Dec 2024 23:00:46 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d63327c55903230272e828486ae5aaf957d092385fcebd55ffa1659d6615380`  
		Last Modified: Sat, 21 Dec 2024 00:59:14 GMT  
		Size: 19.3 MB (19297589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba73d03a2253f01cf4e96ca1ce531ee1bc890cd692a5d0bb33aa5d6a597663`  
		Last Modified: Sat, 21 Dec 2024 00:59:14 GMT  
		Size: 19.9 MB (19941596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25548161c3a4e9f0a26c20c4db3a02b016864382ba545848469b748f4e899bc`  
		Last Modified: Sat, 21 Dec 2024 00:59:14 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c6c7914fb3d794d20311766e3af154e9b463d4555ef2eecd72d106591c4c3d`  
		Last Modified: Sat, 21 Dec 2024 00:59:14 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95ea36d19bcc257124ff290e6df5fe70fb3185b6e99f16e78cacf40b2103337`  
		Last Modified: Sat, 21 Dec 2024 00:59:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cf950957e0eab6d74ae354f32ccbf1a6ba0f4cba70b3d62fb4c515634613b1`  
		Last Modified: Sat, 21 Dec 2024 00:59:17 GMT  
		Size: 205.5 MB (205496446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368bd9ab9a77bf6fe65c4afaa7a9aa0cd741d7ac81bb5ea8136ade41bce8418b`  
		Last Modified: Sat, 21 Dec 2024 00:59:15 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fcfaa9541ff67be08e32a8d1923331fde0766dd70c6b76cc96c38457fc0b48`  
		Last Modified: Sat, 21 Dec 2024 00:59:15 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:da06e90ad40b3d98c37f5ddf857d902db6ad7083fe6a9b2ad9530a782227268b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 KB (60967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd90e44521d8e3f5fd6e7121edebb116dd23bd3603af1252a8eceacd0219e8ec`

```dockerfile
```

-	Layers:
	-	`sha256:0fc3bfdf52e72a45a9c7e4668674444112a27d4969c9d47cb5d3fde0af83fb00`  
		Last Modified: Sat, 21 Dec 2024 00:59:13 GMT  
		Size: 61.0 KB (60967 bytes)  
		MIME: application/vnd.in-toto+json
