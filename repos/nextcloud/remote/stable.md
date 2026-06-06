## `nextcloud:stable`

```console
$ docker pull nextcloud@sha256:96f8b6ad4adf4044ac6d3cbc10ef99b4897c90792782b5b60a5700e5b1b97b84
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
$ docker pull nextcloud@sha256:613dd7b0f01f860c503571f3ce22b057cbd23b7e0ecea261ed606c6f4f52d9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.1 MB (503112629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bab1eaf408c10ffa350f95d9433ee9da3f22b8dae0a20d2445f32da63ac96e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:39:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:41:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:41:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:41:57 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:41:57 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:16:28 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:18:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:18:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:18:22 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:18:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:18:22 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:18:22 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:18:23 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:18:23 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:18:23 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:18:23 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:18:55 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:18:55 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:18:56 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:18:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:18:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2f07689a8ad2be828279559aee2d6217b59dce1c72812d9f1f99c46e83e3`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00af46a6fb8d65b4c2cd5136c18b998028dbdb4724e88728a803eaf1d9bbecb`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 117.8 MB (117839883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ed921f0d21f57b3c511330dfafa30f7a598848ad987b6efd843aec0a6def0`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ede3a51c79f8280b31d50617fad94e5e2f3990fba30ffc8bfe32d5236c2dd7`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 4.2 MB (4227864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223b96e16b4976bf5a9ad173107c1f4b197c6f8a90e0c76ac31b0c05c3588a6`  
		Last Modified: Fri, 05 Jun 2026 22:42:18 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0253b1139356babd7b596fbd44778193a283e0ea1529839ce01ad00d846e7a38`  
		Last Modified: Fri, 05 Jun 2026 22:42:18 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3166beeb233be6875c4147cc838995077dceb1627063e0c253b76be1a852d96e`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 13.9 MB (13898678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405a149b5346b0287a179a63ded29b93cc303c6e4da9df237aa5f7663a3831b8`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba30ea08bda1a4cc3213719a634028d2fcec91aa30b2ec9e4c619720fc155ba`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 13.7 MB (13691044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7806628a945adad88843f81e60ea823b6eb8acb6e29bda1b00268f1a7fca51c9`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6df911884cbfe0001ee99fb42df5721698c99e8dd5bb1af062bdd520fed721`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac6491fcdfec5ee6a149377ee56ef4a2ba5622d8bab357ef5badbd58e1df1dc`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d0b50770cf8181da2166dd5de8426248951e3f11b385c311a0c1a5124a076e`  
		Last Modified: Fri, 05 Jun 2026 22:42:22 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84288cd82467986834c7cec94113b6d71d2208e6e9baf8838cd517f7cae6c558`  
		Last Modified: Sat, 06 Jun 2026 00:19:22 GMT  
		Size: 21.0 MB (20961136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ef18ef8b3f7878e58c54516aa39d413964eaadb813421edaa11afceb2f8d7e`  
		Last Modified: Sat, 06 Jun 2026 00:19:23 GMT  
		Size: 36.9 MB (36894512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3ac6fbd28bb8778197a38706143403e68c2886c55c01292c19bcd59825d761`  
		Last Modified: Sat, 06 Jun 2026 00:19:21 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ca868fe1f5c13f5d0f18ac5104dccb7d4f5aeba493355c4386b6fed5b059ca`  
		Last Modified: Sat, 06 Jun 2026 00:19:22 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c4f3cadfa5e17bad2d5c8b1eae7d24777c1426a378c869e56d93c3e032e03a`  
		Last Modified: Sat, 06 Jun 2026 00:19:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f7425f4cd3b52d2b7187ea7b6c0f92da70fe92190ce2ff919c459274db519a`  
		Last Modified: Sat, 06 Jun 2026 00:19:32 GMT  
		Size: 265.8 MB (265805559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f130772c956d330e4f69df76b2d0ab44ee2debf45221691265edcc9a135868`  
		Last Modified: Sat, 06 Jun 2026 00:19:24 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b0bc1fc79e14addf636b7978cdd1acc9375bae0d4dca8f616119762a46fcc`  
		Last Modified: Sat, 06 Jun 2026 00:19:25 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d62e4a981b8a5220cacb512ce30e494a460f31a6d7128aadb487fdc9a4028000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633411e173b0fd4763e5f7708a1b26eb52740c74a6062da4298b4f688ecac3bf`

```dockerfile
```

-	Layers:
	-	`sha256:fbcd3ba1a90b2bde6653bc8db13a1902c51eb42e7b8c96948edf85d8713cc2b9`  
		Last Modified: Sat, 06 Jun 2026 00:19:21 GMT  
		Size: 64.2 KB (64188 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:1fb86b11fbb5221680fc43954c64a26557c891b79e2ac528e2dcb5675314d50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.1 MB (474060775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6cbc370590a2ec6a119a9950fa6fb5c59fa23f0d1df0055df49312e467f942`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:39:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:57 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:40:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:40:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:43:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:43:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:43:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:43:20 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:43:20 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:20 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:43:20 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:43:20 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:15:09 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:18:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:18:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:18:17 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:18:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:18:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:18:17 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:18:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:18:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:18:18 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:18:18 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:19:05 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:19:06 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:19:06 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:19:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:19:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20c97aed179bfb864ac61b7e17ae90957e42afe4b7ad4fc0328f9e5c223ac15`  
		Last Modified: Fri, 05 Jun 2026 22:43:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2e54ca5c69cde6f1a44500be890fa0aa6b1a8ae4d7551ad74b26e6c1c83a97`  
		Last Modified: Fri, 05 Jun 2026 22:43:41 GMT  
		Size: 94.9 MB (94885711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cd13baf75c2bfe8b7f79ebabc610fbedb175a69331df19540c1d18694b8ac0`  
		Last Modified: Fri, 05 Jun 2026 22:43:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0cabb95db5343768a5fc90a6c61565c71621ffbb7c64f422f0085b91e06eb7`  
		Last Modified: Fri, 05 Jun 2026 22:43:39 GMT  
		Size: 4.1 MB (4090302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb5dfcc59f9b167e787a02f8614418637c72ebb645d77ab264edeb9181f94e4`  
		Last Modified: Fri, 05 Jun 2026 22:43:40 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67aca0494ff0c0ad7e4959272c6596806534f2a81952e8eb7991e9332008694`  
		Last Modified: Fri, 05 Jun 2026 22:43:40 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aba75ebc8c107e33316b4a018bb85b4a69b5465cfb3b4e0c3baed173c1301cf`  
		Last Modified: Fri, 05 Jun 2026 22:43:41 GMT  
		Size: 13.9 MB (13895845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e000b25434bcf17b5782b0d9c411845989e0a7379c9ba9c064cdfc74612cb41c`  
		Last Modified: Fri, 05 Jun 2026 22:43:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f830833dc7fce2169a27bb31f51ee9c278965706db0e1e65f889358f89c9ff7`  
		Last Modified: Fri, 05 Jun 2026 22:43:41 GMT  
		Size: 12.3 MB (12297687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e116afaaff34f1951ed068d118be05bd39201fe071ecb46fc3d65d46a96bf1`  
		Last Modified: Fri, 05 Jun 2026 22:43:42 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b3e52af0020ba49a040aea6a0d84920cccca8f1605f4bc3c97b4c3ddab0eb`  
		Last Modified: Fri, 05 Jun 2026 22:43:42 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55e6fad965e2537478e0b5f23443f25376aa070501e2788a0db565896ee95c`  
		Last Modified: Fri, 05 Jun 2026 22:43:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ceea0c97b281ef7c4dec2cbb992813b00b09900723d9e794a85ec48bbc641a`  
		Last Modified: Fri, 05 Jun 2026 22:43:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfac276418cc6e57cf6f172aada4f74143f8d6c20f672d77e9ca4e8f0d5cfd73`  
		Last Modified: Sat, 06 Jun 2026 00:19:33 GMT  
		Size: 20.1 MB (20061527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e22ab7a11d1100b4c0bbfba5a9688897a54fb2021a8868b3d6075d288c140b9`  
		Last Modified: Sat, 06 Jun 2026 00:19:34 GMT  
		Size: 35.1 MB (35058987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc685b6fa6e95406a93e272b53b16f27ffda293553d15ebdd81314c14c870d`  
		Last Modified: Sat, 06 Jun 2026 00:19:33 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a3d92623093248e95f4d09c747058aa3124e8eb2a279f9d65b96258e1767df`  
		Last Modified: Sat, 06 Jun 2026 00:19:33 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80124affe5fc8ee5a2dde99afa4bbd8cbcc42c8aec633560db1c6f2b4b9b9d3`  
		Last Modified: Sat, 06 Jun 2026 00:19:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb518625e142d00b1ae5e43747f9d7e72c46338e7228bac51fd5378984aa6d88`  
		Last Modified: Sat, 06 Jun 2026 00:19:40 GMT  
		Size: 265.8 MB (265802778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5d7afd08e40385cd476dbf15ae7b9b4104d2454de16840664a349ff87579ed`  
		Last Modified: Sat, 06 Jun 2026 00:19:35 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d4de6f31c2cf11075f415ea6b8bf15f1047a9b8ed1756d564a6f1ba35038b6`  
		Last Modified: Sat, 06 Jun 2026 00:19:35 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:0b0f33ad7f34dd72a6db2541d18aec96f814684255df4d636767a2cc743b24c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a5f6a7608ab630284f8a00bed77a21761d7b916aea02ae871907c39e569cbf`

```dockerfile
```

-	Layers:
	-	`sha256:d73bd3696d37a9034251b298e61cd7e396c2d1632358f83f6014e707443e3ff6`  
		Last Modified: Sat, 06 Jun 2026 00:19:32 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:d695e9988d23959b6d608a2349c2a38779257b2824fcd703e78e41260b0f065e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460290654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcaf775d58225a12827147144ca29ef03374ad2dc765841e79f17709012391e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:39:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:36 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:47 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:48 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:48 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:21:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:25:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:25:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:25:03 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:25:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:25:03 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:25:03 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:25:03 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:25:03 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:25:03 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:25:03 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:25:52 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:25:52 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:25:52 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:25:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:25:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef49eb4129cb389ab49a4d1edb009a8397667aa1a5a5a25c5fe09d2555c0e4fc`  
		Last Modified: Fri, 05 Jun 2026 22:42:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6367a2b5c37154791cd30e344f8752ad05592a3f102084d184ac119bc6d7950b`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 86.3 MB (86256157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9309e35ce84e354961e3afd02de3a72f241f3b1460a323eda422c15b695543`  
		Last Modified: Fri, 05 Jun 2026 22:43:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d964487f564b6dfeadb20c5fff09fe1df38a6c9d46fd37ad133bf8918e53f`  
		Last Modified: Fri, 05 Jun 2026 22:43:05 GMT  
		Size: 3.8 MB (3756685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c06cdcd530eb203db34b94a8afd9932168fbae523ea2c6e8a8ce886a4af733`  
		Last Modified: Fri, 05 Jun 2026 22:43:06 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113509df834836f0475b5a2f2e19589fa95bfe00c206ca57094305cc15bf8c32`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f4de93d6be1c989b55a76daea334c3fcb1409d7fd9438d45d45579a94b744`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 13.9 MB (13896005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e4225a6ba24de6db35f1b12a6e46e90302e7d5ccab0c77dbeb54901ef6d6c8`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45aa4ee8f5c467421c32a6e5a246f174accf76c226b5069e7d63b5d8f61f19`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 11.7 MB (11712268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495d0bfbc535f696d03f3c519b27abeb5ecb8c8bfdf3329ae9da3bb9e42f302`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93caf799ddda63f51f7a21efea228ee1dfbdca9b9ae13fc553bfcb0d000ce346`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459f7a2eb197aef2c8c84366628a0402c16e3aaf4e09486cb0c05a5658f89287`  
		Last Modified: Fri, 05 Jun 2026 22:43:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f37676ccdb442a364c69c9d8896b4f91526107a0d6e4b649a158fc6bfd0160`  
		Last Modified: Fri, 05 Jun 2026 22:43:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92fbdc41b78a23f35c660263e22c32c7ffae298222db22adecf57378468197f`  
		Last Modified: Sat, 06 Jun 2026 00:26:20 GMT  
		Size: 18.0 MB (17996519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04670d8dcebf8152d102d5a71e11646a37e48e84d22a9e5fef405b267d06bc3f`  
		Last Modified: Sat, 06 Jun 2026 00:26:21 GMT  
		Size: 34.7 MB (34650080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cfe675ae52aca5d8cdcd9c8d0ece67a087473ae53701a78b4acf459e3ba50d`  
		Last Modified: Sat, 06 Jun 2026 00:26:20 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8bc3bc47a72b962eed019ba933d86f0455a8c4f1eaeb1002d818670cde2128`  
		Last Modified: Sat, 06 Jun 2026 00:26:19 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6e3c5cfa850b05ada80cf75a37721f6a9aa8fdb7b56683080469b250775c59`  
		Last Modified: Sat, 06 Jun 2026 00:26:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b839136055b89e533330e427d61b7028066ff6da08155d190793e9909418f`  
		Last Modified: Sat, 06 Jun 2026 00:26:27 GMT  
		Size: 265.8 MB (265803061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ead0bfb2041b8af174be202d2482ca5000ab860fb67544ede6be7ac65adc587`  
		Last Modified: Sat, 06 Jun 2026 00:26:22 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b508cf6607eadbf359f66b8f0da4e6932974c5d9a8556c0272d21514ab0eaa`  
		Last Modified: Sat, 06 Jun 2026 00:26:23 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:a494b5757dbc2642203f22dd1716842ee88b5f9bee10b94ebe183a31f0686d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4403aeefb1e71f856afa0ed210a7fbb1036c2a0c6818aaf85af5760863aa5d8`

```dockerfile
```

-	Layers:
	-	`sha256:e1985d83c5d0a93cd9f72610cd691d5b416f630d2cb39b3537b8a57a321807ec`  
		Last Modified: Sat, 06 Jun 2026 00:26:19 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:a13c3b86d900241479f219c5013f0b107bb7e72d99699a8e32284353f938c4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.1 MB (494149851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f530a9f3fbf79b4cb6c8a14c1e31bea4945c1144bfc68dce5dcb1688436f4be1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:38:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:38 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:38 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:38 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:17:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:19:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:19:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:19:48 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:19:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:19:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:19:48 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:19:48 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:19:48 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:19:49 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:19:49 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:20:32 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:20:32 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:20:32 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:20:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:20:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ca734afc06998cc4f469d46d7ea72ebe993b64300582fa19dadf760777d16`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59526dcf80a0c0a7c37013ed0742cbfd2896a4817db99f2bf2a4c5de829dacb9`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 110.2 MB (110169134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0476155b25748c07c80dae6490653f5e448ceec83aca078540f2a445829b1c7`  
		Last Modified: Fri, 05 Jun 2026 22:42:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7e4e26cbc5e7ec40f197b561c548d521ad703e9c12dca6ced20f8c1b64273`  
		Last Modified: Fri, 05 Jun 2026 22:43:00 GMT  
		Size: 4.3 MB (4308172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aed88e2e78ce24c3af427e303d304b2f871abdef109566e0d94a32b91ec8a6`  
		Last Modified: Fri, 05 Jun 2026 22:42:59 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0812317ab085f405383e23b0f3d4ecc4929ef770fca793631e3be7e94f600`  
		Last Modified: Fri, 05 Jun 2026 22:43:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2b825dc1b8409e1bd52d7a3b3eb1a9b371a6ff431a86b8244e717bb4ea13bc`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 13.9 MB (13898308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323b6ea7172ef2c98c5d34dc925223748bf5bcc4fb844939e9b4e229ef517c2`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0c91725ddc70a56d006a136b82bc420ea438a86760ff5697a6843df5090c49`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 13.3 MB (13338628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f79777aa9c5694485f0fd5c66481eb57912a5d866cb94b83c1dbc3c7ac36d81`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b2d572ceebb95ceafc03d938614476c4d6dc4b6b6269174f7df9f271ae4c1`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3a4c5525c34dcb8f795daa01a06232d5a8ec5744f7ea32a24a680bd37dd97`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c81cd241d73959c6db6cec284b640d26831e691013fa670935c5d93f4f9bea2`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a434bb8bd01f65a86a5241bff15ba1d1943216ce6762deb39a8d658b8c13be`  
		Last Modified: Sat, 06 Jun 2026 00:21:00 GMT  
		Size: 19.7 MB (19680988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a3ac3bdc0adc9637794f77ff2270297db8dcfc7a9001a11b85e6e07fae5910`  
		Last Modified: Sat, 06 Jun 2026 00:21:01 GMT  
		Size: 36.8 MB (36793570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c1778dfc702c1c111eea2a3395c5ead0a03c0c55e46fc30d53bda879820408`  
		Last Modified: Sat, 06 Jun 2026 00:20:59 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef304754bbf0ffd24d24c979c37b07a57a976c985a52774648f33e01b20ffb`  
		Last Modified: Sat, 06 Jun 2026 00:21:00 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee05a67d6619aabac9135887e81e8535cff6f231a476a91b568be729d7fe6955`  
		Last Modified: Sat, 06 Jun 2026 00:21:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0cce255a31bd4cad9cffe08a26d27d0915ceaee28f61950d9265b01cdcc8c0`  
		Last Modified: Sat, 06 Jun 2026 00:21:07 GMT  
		Size: 265.8 MB (265805088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8021e0d06fd3cb60c981841e9031445f6fea65547a61d10f70db18df948e331`  
		Last Modified: Sat, 06 Jun 2026 00:21:02 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6a6edb7cc23cfffe17ba1b413f52aff9f77f55c98f879d4ed2628d58b23ca`  
		Last Modified: Sat, 06 Jun 2026 00:21:02 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5959ffd560bebe0e8d7fb862b9fdead3c524d6041c93b547c36a4102c3981042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8286bb024fda382cc1df99d256eebd44b96d81eac51a3668579540b9037889`

```dockerfile
```

-	Layers:
	-	`sha256:184b9aebbb8e11d8d4dececebddb46ff50dc945bfbe2346c76fa669173024384`  
		Last Modified: Sat, 06 Jun 2026 00:20:59 GMT  
		Size: 64.5 KB (64463 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; 386

```console
$ docker pull nextcloud@sha256:1954d902902fc8237ea5ca2620967cc0e7833fdb57bcb7466c19462f3198df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 MB (504118654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fddffcc8a77ed93495a8e7beebf1f237e9efd5a04d8da708578fd0961a88ca6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:38:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:07 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:07 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:07 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:16:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:18:44 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:18:44 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:18:44 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:18:44 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:18:45 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:18:45 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:18:45 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:18:45 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:18:45 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:18:45 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:19:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:19:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ca734afc06998cc4f469d46d7ea72ebe993b64300582fa19dadf760777d16`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d740fa7e6837d80b1e04704f9c826afb84614d0ae758f8904665acd449aafe3`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 116.1 MB (116142193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da462e12d196369d393599d669ddfb1524d415a8d36fb2ce1390b2f05e46f343`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602c55c0f71750b4b8a70c5ac33b7372b06f1754c15a97b1db5720faaf2f6d8`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 4.5 MB (4459159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef107ef7934abace6976310ecdfe9596971080576c11a4e885cbcb201b7cec50`  
		Last Modified: Fri, 05 Jun 2026 22:42:27 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64c752c2c00bc0341d336eb708f0edb8577f364587e49b997637be91f51863`  
		Last Modified: Fri, 05 Jun 2026 22:42:27 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf8cad72ee668d3bc49d93323d01860360678ab389d9ebd57706a0b1d5a27eb`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 13.9 MB (13897515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2363aa8225c0535ea2d19e7c744a722c019e5e7577aa677c90aaac99bbf44c6`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc5078b97fdabfb77ccc5a379fddf75f58e181f8094a06d5adca56f45c1d55`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 14.0 MB (13988055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a60493158bff33ed907925f5b7516f927a9bc4af4c1cad7a28a80ae463ee73`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d8f67303c7306033e175897c5840ef369f3d0437d3f32e7a0138b24c6295d7`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3512886fadf9d7fbc67b7f5289e56439af41d1755a7db5829b053cc2993ca7`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464ea7db1775cb7c4c2379aff6ef7528001daafb896c2e2d88e622766c192d4`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557b037209cf90e3b2bbb552fc9abf6414dbf44069d2ab5b7c3d091a7f41898c`  
		Last Modified: Sat, 06 Jun 2026 00:19:52 GMT  
		Size: 21.2 MB (21213389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d75019e2bdc502d2760484a67ea14dbbaa1f9334c8d65e418e88e89e489b1e`  
		Last Modified: Sat, 06 Jun 2026 00:19:52 GMT  
		Size: 37.3 MB (37304417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba78fee89265e16023647fb80a0d6e0f16631e5859c2588ab1d91e28c941f40`  
		Last Modified: Sat, 06 Jun 2026 00:19:51 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e6545cfa05a7a25e612b90245d518083da1e7f91a122144711620a11a18f9a`  
		Last Modified: Sat, 06 Jun 2026 00:19:51 GMT  
		Size: 567.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6efa59be8c0b0e8c18b2072b66e0d97661404d6a7717500170830d4bdf383`  
		Last Modified: Sat, 06 Jun 2026 00:19:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f8402a1c0eb1fc549173f12f2393f61ae3d372587ab35cdd5af96bb3810710`  
		Last Modified: Sat, 06 Jun 2026 00:19:58 GMT  
		Size: 265.8 MB (265804558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cf8a5868c21d26f64182ba4e498e9f655acda1fa52f997675747b8e18d7b71`  
		Last Modified: Sat, 06 Jun 2026 00:19:53 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd6b4299543bc503aaeb055b12354e575e305dd8f17a223322d7a3c029740e6`  
		Last Modified: Sat, 06 Jun 2026 00:19:54 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:73987288793678620649ae1b6c1c4a2c594f00c66736f608803705c16c2c8510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 KB (64106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e776c50f4785a31b38523716f300e3d2fe41699bd2dd11d31c08c760c14259c4`

```dockerfile
```

-	Layers:
	-	`sha256:b8b52ea9524f3197725c5a5e0e937dffca027355c24653133e9ea79505304168`  
		Last Modified: Sat, 06 Jun 2026 00:19:50 GMT  
		Size: 64.1 KB (64106 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:e9c34cdf718f653ca66cf1d30467880ab793786bb317c0a10fc0ad66bd68dc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.4 MB (503363883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770f37e5ffe9556cf6dafea225e0a54974e5eff8a9c859a50122c95eb15ec58e`
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
ENV PHP_VERSION=8.4.22
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:38:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:38:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:43:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:43:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:43:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:51 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:43:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:43:51 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:50:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:55:50 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:55:50 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:55:50 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:55:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:55:50 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:55:50 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:55:51 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:55:51 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:55:51 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:55:51 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:57:05 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:57:06 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:57:07 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:57:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:57:07 GMT
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
	-	`sha256:9d2e5f6a80b46b08a6e4c44005092a44282dd4f852c4e75710a8baad958376a7`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 13.9 MB (13913049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb74339744d2bb31e8fa8a58dfdee161ffc46c70022a1056a126d980b8acb39`  
		Last Modified: Fri, 05 Jun 2026 22:44:13 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d4f87f2add2b3569b179f01fa8ab12367c102f8de4fcd9da9b2ad095625f3`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 14.9 MB (14933963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b576e37457d6a6a9446c9126a625daaa8b4a7a0607c626bdce9ab3c4ced30`  
		Last Modified: Fri, 05 Jun 2026 22:44:13 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f65c0f891b405eadf31d0b9a99fb78dd88c97ae9d31d3219797d54df73900b`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e88062b15a9aebc5978fcad77bf0e1f72a4e49e54fffbebbab76822269a1`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c010a08a8429ebefb875f77de8d5332019ecee75ce7d7ad84188956471d3761d`  
		Last Modified: Fri, 05 Jun 2026 22:44:15 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9555fd8ad597398552415b6f5f3204fa50ff64037a73ecff7ffb96a1560957a`  
		Last Modified: Sat, 06 Jun 2026 00:57:56 GMT  
		Size: 22.0 MB (22030987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a924f6aacbf061638b015d150ac363164aa74ce13294673b2c6f48aeffe65e`  
		Last Modified: Sat, 06 Jun 2026 00:57:57 GMT  
		Size: 38.6 MB (38583300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c6f69dda31f1f892ced19ce923b3404b5a05cbbceae3366c021328daeba89`  
		Last Modified: Sat, 06 Jun 2026 00:57:55 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e278b01631bca6ec346ee851a3f96f7bb193c63321ad060990669d4914a6430f`  
		Last Modified: Sat, 06 Jun 2026 00:57:55 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84105b44316ca5a860335a1c8c9a8d283e7ec8a5849f18702eec4c45948c19fd`  
		Last Modified: Sat, 06 Jun 2026 00:57:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2ab310f01682cccfc8e618799e8fc64b5f7c93acdbf929f8783a1edc794b82`  
		Last Modified: Sat, 06 Jun 2026 00:58:02 GMT  
		Size: 265.8 MB (265806314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99be213fa80d59640bf1bc16e0171acdc30e8e1cb95a6685794a62b6aa75bf8`  
		Last Modified: Sat, 06 Jun 2026 00:57:58 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2fee6551d2562d8158fa5cc30b1a5882447a764d3d204e078614966aee26f3`  
		Last Modified: Sat, 06 Jun 2026 00:57:58 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5d0cbbe28833ffcf7d42909110c0e237c1df349132df54a941cf88151ca6771a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5549ab34a360d602fbf00b4236f3463f06c77f5ed0ee7b845e7a2a65c77f44c`

```dockerfile
```

-	Layers:
	-	`sha256:e951f92b81b3a59347875640af0d3a161453bd2f75702a32f65415703904df18`  
		Last Modified: Sat, 06 Jun 2026 00:57:55 GMT  
		Size: 64.3 KB (64290 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; riscv64

```console
$ docker pull nextcloud@sha256:25ef3b1a6bd8d502e79cd6f9141c7c7c4f5895d3bc911f38858d790d2adc5696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.7 MB (537686363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaa9fe4d0933f995431f041edb4e96ee43272136ca972f25061f5e0e683d924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 11:59:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 May 2026 13:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 May 2026 13:07:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 May 2026 13:07:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 May 2026 13:07:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_VERSION=8.4.21
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Wed, 20 May 2026 16:58:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 16:58:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 May 2026 17:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 May 2026 17:53:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 May 2026 17:53:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 20 May 2026 17:53:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 May 2026 17:53:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 May 2026 17:53:21 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 May 2026 17:53:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 May 2026 17:53:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 17:53:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 May 2026 17:53:22 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jun 2026 19:25:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 03 Jun 2026 19:55:25 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 03 Jun 2026 19:55:25 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 03 Jun 2026 19:55:25 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 03 Jun 2026 19:55:25 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 19:55:26 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 03 Jun 2026 19:55:26 GMT
VOLUME [/var/www/html]
# Wed, 03 Jun 2026 19:55:27 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 03 Jun 2026 19:55:27 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 03 Jun 2026 19:55:28 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 03 Jun 2026 19:55:28 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Wed, 03 Jun 2026 19:59:53 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 19:59:54 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 03 Jun 2026 19:59:55 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 03 Jun 2026 19:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jun 2026 19:59:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3f1ce6bdb422619d5f28f3d354ac88efadf525446aa4cc0a2cf6d208358da0`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2278d8aba6744e8388864d93d2ccd060b4b5b706da0855420292afc7562eef8`  
		Last Modified: Wed, 20 May 2026 13:05:36 GMT  
		Size: 146.6 MB (146584901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f680f6a3aa4a44306703b8a92e46d186729d6e1435771fbfda06e18de5ebcc5`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887cf26ec25a917a3969775023d91d64e52e0fc30b0f1e2c5a326ce664b36942`  
		Last Modified: Wed, 20 May 2026 14:08:12 GMT  
		Size: 4.0 MB (4031581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e116995318a8f16f6dd281e40820dba3f5cec3ccbf8b001b5f77cc47621731c`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c0690c9ca74d867f3cd4b9dd3884b132b21d1a7e60c2dfcd33fecaa0fb76f`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb8d8473f429d1899ae9a66d74ac649566960fad2512103a039bd145299d`  
		Last Modified: Wed, 20 May 2026 17:56:32 GMT  
		Size: 13.9 MB (13899334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e97986499b5bd8ad4602e6f6efd534682085aefc6287feb6283505f8e4a9fb`  
		Last Modified: Wed, 20 May 2026 17:56:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ad67a97e628d7f2624ece666db5123b0baec686cf00603d125ccd2459669bf`  
		Last Modified: Wed, 20 May 2026 17:56:31 GMT  
		Size: 13.1 MB (13101683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e236ddf49f2bc808108ff595ef54a122aa160929af2620151ed343b64fcdd0`  
		Last Modified: Wed, 20 May 2026 17:56:27 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98015a82670d958c3a1e6cbc3bca2c4436803615665101c4022d6ab79bbd0e79`  
		Last Modified: Wed, 20 May 2026 17:56:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d578448e323d7a6db0e3d4148efadaaace5e141b941127a938ef0c2c114dd06e`  
		Last Modified: Wed, 20 May 2026 17:56:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2a1e75da4aaa5d2dc8930b19927e7c4473a3d0816e5a6c2e1e92ae48dda1b1`  
		Last Modified: Wed, 20 May 2026 17:56:31 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a0e83972fba05ab3b7daebb954d85e5a52d64cd9febbaa396932ebb36ab423`  
		Last Modified: Wed, 03 Jun 2026 20:06:30 GMT  
		Size: 19.5 MB (19453231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d26b28c7be2df8e99a133b7edf70bb6baf7ffe5fb43f2ea27ddc6abc8640d8`  
		Last Modified: Wed, 03 Jun 2026 20:06:38 GMT  
		Size: 46.5 MB (46517784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c9a3730f0c665399639fcd3783132d8cebe489fbfa2f60097d81aac5b2695`  
		Last Modified: Wed, 03 Jun 2026 20:06:23 GMT  
		Size: 801.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817a4bec8af7093f4477b03c874d6d1bc9962b4a61b30bae51ab6a36ffe470a7`  
		Last Modified: Wed, 03 Jun 2026 20:06:22 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1dcbdc2ff8aa8821b18bd751391bc3de5d11aa81618b4b05e05b3078f5d844`  
		Last Modified: Wed, 03 Jun 2026 20:06:24 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0f2dc145c7ccc99991359659195e48ae62bd7914390090d19613665a51a7a3`  
		Last Modified: Wed, 03 Jun 2026 20:07:10 GMT  
		Size: 265.8 MB (265806162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dd7394463bc5713f64b51e7da3b44a5a083d40ead214c9438df1d47017f9b`  
		Last Modified: Wed, 03 Jun 2026 20:06:27 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a6309c4bb2e30389b6401556678dbd95ab16398bd12d59986c8e65916ca47d`  
		Last Modified: Wed, 03 Jun 2026 20:06:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:f58a3ecce10f3004e6edfacece075cec7ee3dc3fcb189fe1131368c9c01b3e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743110099d8fda3cb6e912d3ad38210fe0eb7598ee31286b6478f382f031751d`

```dockerfile
```

-	Layers:
	-	`sha256:046b71351885aa32b7d6c762127fbcc13f79115abdd846649963394ab2c37403`  
		Last Modified: Wed, 03 Jun 2026 20:06:22 GMT  
		Size: 64.3 KB (64290 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; s390x

```console
$ docker pull nextcloud@sha256:e3dacb420c09b78a0a89fb551fdb1d2de7a68d728ada3dd7bd14842417ff25a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.0 MB (477998837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd4f0a4928203c26129f5aaa54d39fd48e9319c7600bdfe9550268162afe1f8`
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
ENV PHP_VERSION=8.4.22
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:38:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:38:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:24 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:24 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:24 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:25:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Sat, 06 Jun 2026 00:27:29 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 06 Jun 2026 00:27:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 06 Jun 2026 00:27:29 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Sat, 06 Jun 2026 00:27:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:27:29 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Sat, 06 Jun 2026 00:27:29 GMT
VOLUME [/var/www/html]
# Sat, 06 Jun 2026 00:27:30 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Sat, 06 Jun 2026 00:27:30 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Sat, 06 Jun 2026 00:27:30 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Sat, 06 Jun 2026 00:27:30 GMT
ENV NEXTCLOUD_VERSION=33.0.5
# Sat, 06 Jun 2026 00:28:05 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.5/nextcloud-33.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Sat, 06 Jun 2026 00:28:05 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 06 Jun 2026 00:28:05 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Sat, 06 Jun 2026 00:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 06 Jun 2026 00:28:05 GMT
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
	-	`sha256:56f7bdd7c348c1336403029eb24b4cfc6bf726014f960bbd6847e29db809a653`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 13.9 MB (13912253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e778f7c4eedf2dd20c9aaaed9f625ea8391ea137a2c2b0a3352d696a251d2`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517bd214162a1a413f7f554c5e033938dfaac9f902869f3ba9b03dc61063fb04`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 14.2 MB (14191079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ed4de46510d84a3eaf6ee8c58e8a0b9925a4e11c80ccf3f29887b0273bbf64`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7027dbaa21b5515fda4679f8104c88eef9a35c26bdedd7fe7f3f03ce21c8cdf3`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a662bae0eb4d9b3d9349d22d5cbf4806f3b6313bd0e4325dd7005f1e6567df59`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8027a1444fda70b3209fd01700201147af1fcc1eae4a15b5014a2c09468a2f`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4aa068e3fecd148acee2ef06039cd13fb53e676874ccd96f375eb7c92217dc`  
		Last Modified: Sat, 06 Jun 2026 00:28:42 GMT  
		Size: 20.3 MB (20277794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601a882d2d4e660f13c1cd5826a3e546f7074da2cce722f4cab7ddca1a6269b0`  
		Last Modified: Sat, 06 Jun 2026 00:28:43 GMT  
		Size: 37.0 MB (37049884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89857652b9724e8b5b6b62c49eafc633704e38ae2c6a66c159cc21cfd1e6b190`  
		Last Modified: Sat, 06 Jun 2026 00:28:42 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13e79b4d7ee212472e5aa608e0eb2157c207f7db3f96687f444f1e801e1b6a1`  
		Last Modified: Sat, 06 Jun 2026 00:28:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07252e75531e9fc03e9b68ac617249680f73a61b7851bba94de5dc401c89cae6`  
		Last Modified: Sat, 06 Jun 2026 00:28:43 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b23eb5d2b17865071d564bbeefcf633adc0b71e76acb2387970597d30e2b2b9`  
		Last Modified: Sat, 06 Jun 2026 00:28:48 GMT  
		Size: 265.8 MB (265803980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65c004dabf76962b90e5208aa4bec625fa1ae3da23ed57870b5951c19b10cf`  
		Last Modified: Sat, 06 Jun 2026 00:28:44 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14589e6759725da80d4bed197a506db9fc4c7eb1a2b289c91700aa5ed377a7f`  
		Last Modified: Sat, 06 Jun 2026 00:28:44 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7f3046421984aa6dd02c4f22b3a0cef44b3c2358cb8ba39dc80a17bd4c459cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b11430bf0e23dc6924ec643c84e295be7209099f11c8b20d2629bc804f7c5`

```dockerfile
```

-	Layers:
	-	`sha256:9169ed315be1b723bcaaf2ecfbc60aea3a9e2d1348e7d0cb77071322f6562300`  
		Last Modified: Sat, 06 Jun 2026 00:28:42 GMT  
		Size: 64.2 KB (64178 bytes)  
		MIME: application/vnd.in-toto+json
