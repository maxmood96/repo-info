## `nextcloud:production-apache`

```console
$ docker pull nextcloud@sha256:311bbf89cdb10320673006f141640d69556dcdf8b60eeae5519e7809a8b86448
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

### `nextcloud:production-apache` - linux; amd64

```console
$ docker pull nextcloud@sha256:f2d41fdb3fbb0ffbeeed040df10bafe918e1e7ac9a1a8256c37098ecb874ea50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466847010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64815f85faaca94e475f1ff63600026ad0dc697b07749e452cf00bca510c88fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 00:38:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 00:38:01 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 00:38:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 00:38:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5886df122f3d10b88a37d88cbdbaab47aecf0346719bbf76ac14b654354f3a`  
		Last Modified: Fri, 06 Jun 2025 17:39:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54a66f47a0911da9e95a2ed2a7feb60c2c8346e8207cf1b96f3ee2ba5faefa0`  
		Last Modified: Fri, 06 Jun 2025 17:41:00 GMT  
		Size: 104.3 MB (104326374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f0d2402f4860ef858cf479650ddef1d9ddf1906e91601ea124ff03f0834c6b`  
		Last Modified: Fri, 06 Jun 2025 17:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd024bfd11586a8fb50726543dc0b237eeb98c26f5f515a4d626eee758fe84f4`  
		Last Modified: Fri, 06 Jun 2025 17:59:26 GMT  
		Size: 20.1 MB (20123843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b04524b9bc85bd067ed79a35b798b44c4382f7493eb6585b16fd7192fef081`  
		Last Modified: Fri, 06 Jun 2025 17:59:24 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a3624586002b8b5d75025ad7cf1f663da756d2f552b2db0732d8be2e11c809`  
		Last Modified: Fri, 06 Jun 2025 17:59:24 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efcda5680f4fc39944245b53f4e0b17201c26e4ce7448a0c6ff169db3c85f5e`  
		Last Modified: Fri, 06 Jun 2025 17:59:24 GMT  
		Size: 12.7 MB (12683573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde08ae2e18fc0733f7809813f24adf68de1d9cf456d76a19963aa987187e32`  
		Last Modified: Fri, 06 Jun 2025 17:59:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca778c9d5d037ef73eb64094a20e53cd6f059baa8534dac21708b196286392`  
		Last Modified: Fri, 06 Jun 2025 17:59:23 GMT  
		Size: 11.7 MB (11657835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336e5048d4f7355bfaf2089e35e4ac0e070009d1fd98f424e96b2976e3769aaf`  
		Last Modified: Fri, 06 Jun 2025 17:59:23 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055f25c77bcc45a793a155ebf874f46c598158dc9e8721e4f78763247152519`  
		Last Modified: Fri, 06 Jun 2025 17:59:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9720375f9774bd1231552449ef1c25b46760a9b66dfdaad42182e0e2b8e131b0`  
		Last Modified: Fri, 06 Jun 2025 17:59:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62dbdac9dec65d39190b2a93ff25a88e6601b6c4bd62c4b8810d2bca4a9a29e`  
		Last Modified: Fri, 06 Jun 2025 18:06:33 GMT  
		Size: 22.8 MB (22784762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587970d987e4158a5a63996f4a539416b3141ec9bf7fcef9d656e4ede4340d00`  
		Last Modified: Fri, 06 Jun 2025 18:06:16 GMT  
		Size: 21.0 MB (20957485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ae61164f4429e4fe48ddfb0382c2d15e40d0c69e2a545ba2558e13acd49964`  
		Last Modified: Fri, 06 Jun 2025 18:06:15 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682ee37b9da415e6dff2586d5394708faad801061d324c39f8bd5fada5dec130`  
		Last Modified: Fri, 06 Jun 2025 18:06:15 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac424d7b3ea7f7bafb65f78ea3287ac7cfcbb932d85e1d7716229696e370954`  
		Last Modified: Fri, 06 Jun 2025 18:06:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5102c92f4a01cf5de5b8c19f90682f7e624d782a403e55dde7ec470c39bcf0be`  
		Last Modified: Fri, 06 Jun 2025 19:04:31 GMT  
		Size: 246.1 MB (246074123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77252b5c116f2a3693b710ef932028ded85172e9d265e0aaca2e0aea3f0aa9d8`  
		Last Modified: Fri, 06 Jun 2025 18:06:16 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0c607195fd8b1ae9242ee11ed8e8ea8571bf982c23d6dce6c321e7fa1bcd4`  
		Last Modified: Fri, 06 Jun 2025 18:06:17 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3b1d139399f57bd6f1d0f26a14e354de0a5e325b58914176a300a6945749af43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 KB (62580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c0ac425210fe280504f11417e57a4ea3343b2f0e7ed9dc6b159c07d0877282`

```dockerfile
```

-	Layers:
	-	`sha256:01be521e70134ab295f26d60a41048e8b2e8a151df86b2833fca149f29b414a2`  
		Last Modified: Fri, 06 Jun 2025 20:51:04 GMT  
		Size: 62.6 KB (62580 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:948ef2284b1bec9397b46daa8107b55c513755a2cbbe12be202563029b563cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436080411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeffb527aa4df2cc83a9e9c92ca4282a8572cc01a9acc70ebef13cd4034156c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 00:38:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 00:38:01 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 00:38:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 00:38:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630a0ae6a7caa13c26c641757aedb6f2a685e945563086d454f01db874d5a4e`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1543f1d03f96cc1c05ba7756b5950bbb8edfd3038bc0902f7bd06c8b3a5a6`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 82.0 MB (81970289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1f2e7aca197ce584722af1cb59310256391ea143b4eee91fe64249d0f64ac8`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58b58ecad378e2c244a47b087001bd8dd7a6bb20346f6a44056db42ab3a5ce`  
		Last Modified: Tue, 03 Jun 2025 14:07:07 GMT  
		Size: 19.4 MB (19419290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f2b7224a1481ccb5f31a4a4189cf4eba4409cd5baaf7402ee9bf4a6ba1d7c`  
		Last Modified: Tue, 03 Jun 2025 14:06:58 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e190f82563d835d64144f74a1701508a80fd49ac413b53cda42a431d89cf4b`  
		Last Modified: Tue, 03 Jun 2025 14:06:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30242a306b68dd4b7a955136bf5bd1141834c74540da4be7d2751d6dab53de76`  
		Last Modified: Fri, 06 Jun 2025 18:09:45 GMT  
		Size: 12.7 MB (12681837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a065b00e5cad9130d224efddea082e6e15459c6c5ca367188e424a9e712f3c67`  
		Last Modified: Fri, 06 Jun 2025 18:09:44 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c2fcb06bf88167bc82676bc053db0ea02f223e02cf439b896f33c0b6fdb5f`  
		Last Modified: Fri, 06 Jun 2025 18:09:45 GMT  
		Size: 10.6 MB (10627781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6440c37e671ba0e719296aa12686c2b647a893c2144bba13063088d2bff8cd`  
		Last Modified: Fri, 06 Jun 2025 18:09:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85415ea524f94cdf419e6bd57314bb0f9cbfbcf74e5acde53fbd104952c575ae`  
		Last Modified: Fri, 06 Jun 2025 18:09:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52efccfc60056cbd871bc0fd609a7b415665c8de8b9e299c6020b5ea268ea470`  
		Last Modified: Fri, 06 Jun 2025 18:09:46 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44d84d81c05b778a248c06be17301c55b744f18e12525cc97bd545209d15aa0`  
		Last Modified: Fri, 06 Jun 2025 19:56:25 GMT  
		Size: 19.9 MB (19895842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f0836482914e7f2dcea742e3cf3a42138ec6cb5e40c5f9e55478a165029ee`  
		Last Modified: Fri, 06 Jun 2025 19:56:36 GMT  
		Size: 19.6 MB (19642154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deab890eeb3c59f2520b5deed3404cebc3e554aed20f1fca4808edb5713572fd`  
		Last Modified: Fri, 06 Jun 2025 19:53:13 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca36f5776f8e9852b6f350c8c2f42ae6b8697128e722e2f43abc44d9e83fdb0`  
		Last Modified: Fri, 06 Jun 2025 19:53:17 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98e1f34782fb032bf1372e66272d11dde2903987efab48d102f554ec2c9a4a`  
		Last Modified: Fri, 06 Jun 2025 19:53:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e085839bcd0b1bcbd503cb5049bbf8c44ca658345810f91f94184b1df52d3592`  
		Last Modified: Fri, 06 Jun 2025 20:51:45 GMT  
		Size: 246.1 MB (246072604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b4265fe117f9b10cfdd0278578cd06e3cc7b7a330523263393b16bc8b72138`  
		Last Modified: Fri, 06 Jun 2025 19:56:23 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbc3b8bd0cccf65ab9e7028fc0e8afa8fd1b8e8c4f5644695239cefc8cd51f`  
		Last Modified: Fri, 06 Jun 2025 19:56:23 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3c72d5f018a76b8c075aa0a937777cf15e937a9dce8841b96455556947b725de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d0085e0d8c3adb2747c7dfdcbbd7a58ed6f66f2a966ccdde2d3d49001ffa80`

```dockerfile
```

-	Layers:
	-	`sha256:f3224eaee7e882e524a5810be795c772f50bf80a74aaa5174c3cab8ddede9d3d`  
		Last Modified: Fri, 06 Jun 2025 20:51:08 GMT  
		Size: 62.8 KB (62775 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:c18766f8d3ce4d36c4115e251cb0ed6476130857571e6895648afab72022dc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.8 MB (424844187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032abd78566336bfca5128ff75c2948a737887c643e1579dadf67f3cd26bbde4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 May 2025 22:40:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 22:40:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_VERSION=8.3.21
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 22:40:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 May 2025 22:40:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 22:40:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 08 May 2025 22:40:28 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b0d6d3f419936777d490c71b48fd196b853be826a3cbe2a99f87ce45962a8`  
		Last Modified: Tue, 03 Jun 2025 13:33:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b3dbe5e2b037219e6a37b411897a539f579592c7d55f751f30cdcfee2dafdd`  
		Last Modified: Tue, 03 Jun 2025 13:33:29 GMT  
		Size: 76.1 MB (76132659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56653e4c243acfc3e7a605794bbf2267c510182bd9d2f39f4bcf6a23263375bd`  
		Last Modified: Tue, 03 Jun 2025 13:33:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685993b77f7d52922724cc7923b4ae3c3fca80c6d95d24466f21896fd02e39e6`  
		Last Modified: Tue, 03 Jun 2025 13:35:35 GMT  
		Size: 18.9 MB (18857575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa27ed9872b7024c07a4a56aa9a0f051809faa8364467d10f7af87990268507`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eac574232d2b47fe0f2924dbc13495d266c0790fe259b37113ec8f3ff7451d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37ec7a891fb74b6eb2b39bf344c4aef223ba1785b14cd6c56e8a93e676e1`  
		Last Modified: Tue, 03 Jun 2025 15:00:36 GMT  
		Size: 12.7 MB (12692887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e329c86e48d20c8a1692cbe44d0b3206c1ff40f86387eeaf965b04127a3725`  
		Last Modified: Tue, 03 Jun 2025 15:00:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e2e9254baf754a90b9f137746193f6e4074f48d02daefae204b6e7d5551219`  
		Last Modified: Tue, 03 Jun 2025 15:00:35 GMT  
		Size: 10.1 MB (10052332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7874fc5b297964a6d7f7eaf1819ac05019105724b47368a5a76638d46e2090a`  
		Last Modified: Tue, 03 Jun 2025 15:00:34 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f1ce982e392cc9c7b4ea0e5f401961b8da7aa5bf275345edafac3ed32f821`  
		Last Modified: Tue, 03 Jun 2025 15:00:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda6144c9580c47e55fb0cf766e78f74b35d5907f1db9ab4e11383f0cf30f020`  
		Last Modified: Tue, 03 Jun 2025 15:00:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c689152598cb4537e6c86c0ba836b0a37710759fdbcbc16d14670805922a3`  
		Last Modified: Tue, 03 Jun 2025 15:31:07 GMT  
		Size: 18.1 MB (18146142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b795574952f06a410caaacd8063e1a443a5e7d149af1acd4cc06b8aea8d1230c`  
		Last Modified: Tue, 03 Jun 2025 15:31:25 GMT  
		Size: 18.9 MB (18943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25696bc06fb9350f79ff110b0978572463cfd0c110a49ccad99ce8049a6daa9`  
		Last Modified: Tue, 03 Jun 2025 15:32:17 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6f559f8190b3d6b99a0f5238caa3439e2b349c1848ce1cd7c8ef7b7b2cee8`  
		Last Modified: Tue, 03 Jun 2025 15:32:22 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a51f816060d5cf3a2078f303baa4fde18720b1e4ad190a3f557cd15df7d757`  
		Last Modified: Tue, 03 Jun 2025 15:32:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428446e3d01c30001c51847bbc7479923d6b5ffd88e591bffc505c7f8d00acc1`  
		Last Modified: Tue, 03 Jun 2025 15:32:43 GMT  
		Size: 246.1 MB (246072599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a6099837f8c6ebe4600a49b0e37c860115a8832a9e30b0813ae42a9e131eda`  
		Last Modified: Tue, 03 Jun 2025 15:32:29 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f9cd016c5869fb0db52e40d8d24e9ca6acb4931f24f228eda32e0445423ecf`  
		Last Modified: Tue, 03 Jun 2025 15:32:34 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:0d62aa5cbf2dd9b901e83601fb854bbf484882385b1e494072560fce6561fcf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa885eba817cea9219087eff9856e3acf51b0687c146acad71c0ed7dac59fc`

```dockerfile
```

-	Layers:
	-	`sha256:a500b1c38ffc3eed5f9a11c5cdb5f3facc7c97ea934a8ed5d917acf40a07b3fc`  
		Last Modified: Wed, 04 Jun 2025 10:04:45 GMT  
		Size: 62.8 KB (62776 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:ee7479396386a83c7d6eb24231a76b4ef13c03cf9b06287502cfb67e130c1792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.1 MB (458097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e19913d67b7763070139ec15f7179ae74875a1328b319085c8a74210ea9e737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 May 2025 22:40:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 22:40:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_VERSION=8.3.21
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 22:40:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 May 2025 22:40:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 22:40:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 08 May 2025 22:40:28 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162264c942aa762db417d45ba0a061dc8a07fdceff32a29a2d59afdc5dce9f9`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae464486e7a7b754207a11225be678aa24148395332f33c785867c1ee4adcd`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 98.1 MB (98128413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa473689d317e799934b0b99abeaba5a91da4380c0b6148373000ed23bde9ba2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c2eb5e806f90915c98adca0127759107240352870bfe86a7178c29ff06f3b`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 20.1 MB (20121045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0dcaea15d7a4ebb0f4028699191ca3aa2002cfeec7788806c673ebb001eade`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e656b0988010277ad979af2247a277d3699b9eef4559bbf50725b446fb4510`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348f8a5c7d38ff9d4a6ac85622b907b6638ea2fafb66f642f60a5aea9295c68d`  
		Last Modified: Tue, 03 Jun 2025 13:30:32 GMT  
		Size: 12.7 MB (12694665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb922c0029f681cffc7285553daebf616bef66ed18a0231cc6e0290040db485`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb25ea06c756635811426f88394a1c1cbaa648ba02ec7824b19d7253f685b0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 11.7 MB (11680311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90280cee654716c2503e730efac74700ad9eefc7d8c4773d66c0d20cc6e08326`  
		Last Modified: Tue, 03 Jun 2025 13:30:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29fcacf279cb0fd4697d3a1e0220eaa4100a963bc43a5ea962ce9aa14e8075`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9af748e1436181f47bc7ea7cc9f6539654115603140e9a49de2bbe6235524cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169b5326c6598fa87418bd16e80f2d3274a95f184f117930d1135c739503be86`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 20.1 MB (20145035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3631845f9f364138163cefb366cc83534279aa1d907a97eed790a3d9b0909d1e`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 21.2 MB (21174462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bf170a9cf1980f75be8a3c2e96821246b93095e70984cfc2a6648aaa09aafd`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 797.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc088edf1bafc797b08b7eb101fe54d35da7ed530b25f8e5e9a248dd36dda473`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0664c4c6f90d535c6af33827658bb819494d60a6c7376ee5bb8ad65658b6938f`  
		Last Modified: Tue, 03 Jun 2025 13:30:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d42c2d879871163c817b6c2d5a58a6f38e480bdbe4041b2812cc3b0fa573bf`  
		Last Modified: Tue, 03 Jun 2025 13:32:05 GMT  
		Size: 246.1 MB (246074336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298295b650e50407fe3469c7919d938f29d3504bf166c83bee3d92943baeb666`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b089be85269486c97c53c65fb25ea7969bbe0e541cb12aad1ad5e6c9dfa92`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d723073ce96719ce255b6efe7db8fe2f4eea170827c270161cfab0ac84ba854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8ae8af1c60dc1b8c89624b8ae5062dfc04b8c3886fe72ca6461b7b939c2135`

```dockerfile
```

-	Layers:
	-	`sha256:41e9162c49106d54a60af45ff817aa991e7ede8d6877aecca97dec6bfa0ed0e8`  
		Last Modified: Tue, 03 Jun 2025 20:24:53 GMT  
		Size: 62.8 KB (62846 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; 386

```console
$ docker pull nextcloud@sha256:05e17aec0d4914b7022b511660c71bbb7a134a630f83097bb92559b7343bdfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.4 MB (465446568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0739be994c845c635b577d56f65f3596045f726bb65d0e974761e29205520853`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 00:38:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 00:38:01 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 00:38:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 00:38:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b6c839d57a568da832ed46960b0434ff5facca969332322ce1d6d4a2b906`  
		Last Modified: Fri, 06 Jun 2025 17:41:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51edc83c8c645fb772046b7f5e056458635e10a94cb9d5779485089c1b484390`  
		Last Modified: Fri, 06 Jun 2025 17:41:31 GMT  
		Size: 101.5 MB (101508005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a95cc151fc66bbe5ee285142f79186f0aa685095e329795bef551443310a4f`  
		Last Modified: Fri, 06 Jun 2025 17:40:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897faaf40599059f1abd9544ad9e0a647ac85e9e6dd2b2d900fc59dc55200dd`  
		Last Modified: Fri, 06 Jun 2025 17:59:25 GMT  
		Size: 20.6 MB (20638526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e428ceaf64f243272875ef6142b817de2e8dad9714da02f57563a2f3dd96c022`  
		Last Modified: Fri, 06 Jun 2025 17:59:21 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f220dbeb5d4300f4ba12b2cf30e58b146745deaf8e34a8c351539f174980ea5`  
		Last Modified: Fri, 06 Jun 2025 17:59:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e11e04f76bc9dff0bf3feb376e4c995725037c44d8ac338d6328d85a9e29af`  
		Last Modified: Fri, 06 Jun 2025 17:59:22 GMT  
		Size: 12.7 MB (12682754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01197cf617afc8a9ed042a790da192a4ea4e61522c03c617165403473c8e81d8`  
		Last Modified: Fri, 06 Jun 2025 17:59:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae81fbe54517af3e4733b3b0aa741195aad0f58569522bcebd979b751bd85c4`  
		Last Modified: Fri, 06 Jun 2025 17:59:20 GMT  
		Size: 11.9 MB (11884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da55dd75c152da666203ea407b1313d5e66413d0b355137a9ada2480d8ad096b`  
		Last Modified: Fri, 06 Jun 2025 17:59:19 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237e5c828d466ff0b2f5c8739b5a49ab9c10a2baaa058cf8c155d8bc713e451`  
		Last Modified: Fri, 06 Jun 2025 17:59:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed607be87f28d4c6063a1c351a8474011b13e956cf0e38d12a0b1079b7ef6eb`  
		Last Modified: Fri, 06 Jun 2025 17:59:19 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eee3800ecf82988286db21e280289cb53374fdfb17d66d44284dc5f75e8806`  
		Last Modified: Fri, 06 Jun 2025 18:06:45 GMT  
		Size: 22.3 MB (22263944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700f29478c9fd3e588f58a2fd03de7a2fbe9a56ab6b6f62c31ed7e088a9a7a81`  
		Last Modified: Fri, 06 Jun 2025 18:06:46 GMT  
		Size: 21.2 MB (21174868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fdb730d598bd947a0fa30ef04b32550619347c8b520b70972cb5f4802b788e`  
		Last Modified: Fri, 06 Jun 2025 18:06:44 GMT  
		Size: 788.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163d410998c4127ec5e1b065042ef8f67f5b207e2a4409d98c41beff15f0a9d0`  
		Last Modified: Fri, 06 Jun 2025 18:06:44 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84da0ef981346e86904bcc24294480009ad37154db6a9f28f3f34489c781f603`  
		Last Modified: Fri, 06 Jun 2025 18:06:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13b9f4392c6bcc85c5af07dcf2d53e97b484f4144a1ad19591df340b2fd6b16`  
		Last Modified: Fri, 06 Jun 2025 20:51:47 GMT  
		Size: 246.1 MB (246072993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e34ad026df3e3c35daf8515ca573998123f00428462d1609ee6f158febbc6a5`  
		Last Modified: Fri, 06 Jun 2025 18:06:48 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e14dc342bf69fdb710c5f9bafa8b92bf87205adfaacae704633f05586960b3`  
		Last Modified: Fri, 06 Jun 2025 18:06:48 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:26686ae618c13a3c37364ba5d569b7bdb83082184f731387219c5a8e5cc3b909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 KB (62498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7c7642437e8a3d6a1f228f7bd75816564c75c3239524facb4e4adbc3104f4b`

```dockerfile
```

-	Layers:
	-	`sha256:1464e1f8123c1396a76d214e1834eea5b24345cdac59ddd512e312a91305e4ba`  
		Last Modified: Fri, 06 Jun 2025 20:51:15 GMT  
		Size: 62.5 KB (62498 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:a1cd5bbcde3e6b785ac3c5a905e66136d3c2c67a6c4c33a4a2f811477a0a5955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.3 MB (439293845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01607e586942dac0c337a85f56cabc42fddc4995dfd2bb4b7bd79e68a7c251a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 May 2025 22:40:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 22:40:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_VERSION=8.3.21
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 22:40:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 May 2025 22:40:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 22:40:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 08 May 2025 22:40:28 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b2d065c1ae51e1de38627f7944c17a1a577f385d527b6bf91b589844d0689`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5af86f1704d74588bed3a81502d5b84aaa58ec860f5145be4f0fd74e864385c`  
		Last Modified: Tue, 03 Jun 2025 14:07:31 GMT  
		Size: 80.7 MB (80670380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286f15cd07eee9997888e6110e809261f661823a9bcc233812db970c553fb13`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e479bd14b9daf00989f06fcc9447b78b71f0f81af33588568f8d5514c9dd5e5c`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 20.1 MB (20069286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516d875c6c1a415ec40dd717d030fcbfa51d61ff8a893d36a8f709ff81ba6b86`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b026852626d4fa32104a7a1d8f0f0dc1b9dd3a30a7d8eea66f49a4d583c81`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d510a25c7ba136b8ed5ab8247560faab5dc65959b3211ddc7009c1d4aead4b`  
		Last Modified: Wed, 04 Jun 2025 02:14:39 GMT  
		Size: 12.7 MB (12692608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd1d1deccc872c075794729b3d810a05590f5b00d2e8b98556b3ccd0172431`  
		Last Modified: Wed, 04 Jun 2025 02:14:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa364318f2e510653ee887583a82d47583523de85a9b0a48b1217350bedb259d`  
		Last Modified: Wed, 04 Jun 2025 02:14:39 GMT  
		Size: 10.7 MB (10726927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf78f1d8371041a8cab64996bfa461803c19b1df84985e11e5a0eec824a576`  
		Last Modified: Wed, 04 Jun 2025 02:14:37 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aa943bc90fe569530a8f64ccd8715084443802045249136f0392b80d05dfb0`  
		Last Modified: Wed, 04 Jun 2025 02:14:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c28a15ae5b494c3a338dccd1cd538eff8cb7f68af5c885090b3781b2e1315ca`  
		Last Modified: Wed, 04 Jun 2025 02:14:36 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9c7323f0df9d70b7de141c7dda0cffcfaed76601e2e0606609008fa35565ef`  
		Last Modified: Wed, 04 Jun 2025 02:14:37 GMT  
		Size: 19.8 MB (19804350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9fa8d17c88446be0eaba2a19d4b235b6f1f13b10b64881e3a50179c627f4c6`  
		Last Modified: Wed, 04 Jun 2025 02:14:38 GMT  
		Size: 20.7 MB (20730942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4dec442726ad8bc44de9dcaba5d6abfa1c646e4660437c83428e6f8925f438`  
		Last Modified: Wed, 04 Jun 2025 02:14:35 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6839d590a37422a56afa6362ae80fa5fe7be70d564cb7ec03917094f7e320be5`  
		Last Modified: Wed, 04 Jun 2025 02:14:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a21f3c4386d7d6a3235450d09c6e8f1f6501b1bef1507fe31dc54f515529cf8`  
		Last Modified: Wed, 04 Jun 2025 02:14:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c54b711c833e1dfa23682aec58e34ad65f6b67e3ea9f1383405eb113265899`  
		Last Modified: Wed, 04 Jun 2025 02:14:43 GMT  
		Size: 246.1 MB (246073772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaa09e718bef9308bd3adb360316ce144987c80f311c9db8770bbea62a4fd19`  
		Last Modified: Wed, 04 Jun 2025 02:14:34 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b6b62770f4d8900881dfd2ec5901890f8e80a934dc89aafe3e8c63c146e8e6`  
		Last Modified: Wed, 04 Jun 2025 02:14:35 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:a42eba3eef820914fd7e38228529df16e939837151e9ca82ea05666e9eebf271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81466650affc4bf65a2a8da4983732df1dc8592344c0f24b88b80885a26291ba`

```dockerfile
```

-	Layers:
	-	`sha256:32061ef002719caf261abb084b2b3c06cad689e382eb3ad24fa2afb5b36573b0`  
		Last Modified: Wed, 04 Jun 2025 10:04:52 GMT  
		Size: 62.7 KB (62724 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:e012db62b05979023151a9330252900c2145235f479d9b0cd529c0cf34e528f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.1 MB (472056423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2699e78c6840dbcaf32a68200e5cf1fd8c69ca4cef97ebfe728153fe86972695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 May 2025 22:40:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 22:40:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_VERSION=8.3.21
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 22:40:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 May 2025 22:40:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 22:40:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 08 May 2025 22:40:28 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c8f6558609f4eda938f055dbc23ff092be663afb6bb7d22397dead0d155e4`  
		Last Modified: Tue, 03 Jun 2025 14:07:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95a24f0f53c73df78df26adee8011626da1dd6f4150d1531843c39f2fa7279`  
		Last Modified: Tue, 03 Jun 2025 14:07:40 GMT  
		Size: 103.3 MB (103318542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbbd3cd9d8dd0b29377d19251990f04906ba83ff91eb897513badc4d334a010`  
		Last Modified: Tue, 03 Jun 2025 14:07:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a26aa298acacfff30831e2b7eac827bbc698998de1d7f5e4980067b0e49b8`  
		Last Modified: Tue, 03 Jun 2025 14:07:38 GMT  
		Size: 21.3 MB (21308439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e4c1af0ff654deb6e781136c8bf50cbc1620ff308937fa9386f4e352a660b1`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6045a09715f2b5e30561b3fe36e20f490290134575d98d8260aea00ce45d6`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0661d4932487262312bc79bf118aa03e27798cb9d4abebdd0f861414455d5de1`  
		Last Modified: Tue, 03 Jun 2025 21:47:34 GMT  
		Size: 12.7 MB (12694372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2f6caa1d64902de927e6901ff6e5c62c67003e4295546e3856df318bd271d`  
		Last Modified: Tue, 03 Jun 2025 21:47:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776b6d469e76238eb762b1344f60af4792ebb1cb20931d490ec5e87debd3b9f`  
		Last Modified: Tue, 03 Jun 2025 21:47:32 GMT  
		Size: 12.1 MB (12072469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258a09005daa909e34b8eefa7afec2fb76fd780cfa1f9643384b31c2a588f367`  
		Last Modified: Tue, 03 Jun 2025 21:47:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8c29027020b38e5bd18e35a95ce04415661077f586bcc3a977de442817c343`  
		Last Modified: Tue, 03 Jun 2025 21:47:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9206294a12d45c6bb809e0152fdf09f2c585b28d6b30342217654b7e13f266d`  
		Last Modified: Tue, 03 Jun 2025 21:47:28 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877de02bae808a7fd1f2c4035f426cdd148fcc4ff988bf80b8974887b2fce1b2`  
		Last Modified: Tue, 03 Jun 2025 21:47:31 GMT  
		Size: 22.6 MB (22624768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f39ca955a5b4517fdee6f0b5da2e9ec7f0208793a8405c965594294c845db9`  
		Last Modified: Tue, 03 Jun 2025 21:47:32 GMT  
		Size: 21.9 MB (21882955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d73d6b8cf48d56485c6295199b0e6605d192e60d2ba53ce7c8df75af511514`  
		Last Modified: Tue, 03 Jun 2025 21:47:27 GMT  
		Size: 796.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f17d8a86f5034737bc3061ba482410c4caef92ea1df9a326c3584b9a7dca607`  
		Last Modified: Tue, 03 Jun 2025 21:47:27 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169664d8086f18c4093a5bc582e641894481161eb53533f833402209568c1a13`  
		Last Modified: Tue, 03 Jun 2025 21:47:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa13f8715b7618286ad2b7950e9c01b62fefb41b6015ab7c80ccda4087108357`  
		Last Modified: Tue, 03 Jun 2025 21:47:50 GMT  
		Size: 246.1 MB (246074263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ffbf4da30e0f69759906c0143f5fe3d99e504c3cea8d228ba9da84276c9912`  
		Last Modified: Tue, 03 Jun 2025 21:47:25 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9817cf897b38930927195a448e1bad7fd7700e6a4973ed07316cf594d1169b7`  
		Last Modified: Tue, 03 Jun 2025 21:47:24 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:829b8780e93bb6664c285c82f97b59f768b6fdc698ed9156b0b2bf98e8a108f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4e3e1222deecf42332637bd4677b8d807f2991b9130722ba2f442dda8163c4`

```dockerfile
```

-	Layers:
	-	`sha256:3694246ac438c703dd43668a61880534cb7d89deb52bd4d960a1343fb9c8ae51`  
		Last Modified: Tue, 03 Jun 2025 20:13:48 GMT  
		Size: 62.7 KB (62682 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:367621c386f83f9b93c55680e058ad4e177a8baa8ff5425e194448fff425214a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436708420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e20147bda13c8702c95cb08c41e03d5e5fc3d970d03683b99f3bfa5fc8f5d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 May 2025 22:40:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 May 2025 22:40:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 May 2025 22:40:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_VERSION=8.3.21
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Thu, 08 May 2025 22:40:28 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 08 May 2025 22:40:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 08 May 2025 22:40:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 May 2025 22:40:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 May 2025 22:40:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 08 May 2025 22:40:28 GMT
WORKDIR /var/www/html
# Thu, 08 May 2025 22:40:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 08 May 2025 22:40:28 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 May 2025 00:38:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 May 2025 00:38:01 GMT
VOLUME [/var/www/html]
# Fri, 16 May 2025 00:38:01 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 16 May 2025 00:38:01 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENV NEXTCLOUD_VERSION=31.0.5
# Fri, 16 May 2025 00:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.5.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 May 2025 00:38:01 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 May 2025 00:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 00:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e64042a8c749f17bfb3b660d34f4e07edd06c81899da76f0b866d5592048d`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae504c4e6cef239a74e8e2bc8e65a5adfc4fd86d2ce43efcb6fcf7b948f38c6`  
		Last Modified: Tue, 03 Jun 2025 14:07:59 GMT  
		Size: 80.8 MB (80824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9845dffb4e53bff01a8cc52346eef48b2a105a195a30ab820e7df1e9682a7a`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d076bcc60b618a69a01c7cec130e41e98f5d4ef5c1db46cceb7b121173ee5`  
		Last Modified: Tue, 03 Jun 2025 14:07:45 GMT  
		Size: 19.9 MB (19895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf1bc43a3bf929df811240c21fd8f7c539c8a225d996960c3345d25963bc4c`  
		Last Modified: Tue, 03 Jun 2025 14:07:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aaa5fa23882a5d77ecfeca856eb346385fec09755a18d670b6ceb0cba14cd0`  
		Last Modified: Tue, 03 Jun 2025 14:07:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ac3cbb3ee52181f5870c40d6ff0a1b3c15f7a493834b7ffa858d4ba114e83`  
		Last Modified: Tue, 03 Jun 2025 20:13:40 GMT  
		Size: 12.7 MB (12693285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5a12f32c7ad22ee862dedc750d697163f4baa8ba216508aec32a28c72eadae`  
		Last Modified: Tue, 03 Jun 2025 20:13:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e519b3f987f99a350906f85a83308a333dc3bb83c855c6f8039d2bbe4fecb42`  
		Last Modified: Tue, 03 Jun 2025 20:13:41 GMT  
		Size: 10.9 MB (10877513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f03137a91efb211c66885cb4db54cc38a9ce7daae5ace4b12e9fb71e26971`  
		Last Modified: Tue, 03 Jun 2025 20:13:41 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5738264205b6a2bb25b89a22c01b95a2a2d35399772e753209307f4344d4a007`  
		Last Modified: Tue, 03 Jun 2025 20:13:43 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e03f6ec5d1a9cc5916c74caf43667c2dfcfca33467fb0983bc8c665c61b78b`  
		Last Modified: Tue, 03 Jun 2025 20:13:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d50f41cdc3acd01a50a5e5dc4d4b3365e83e222367cc23ae4e7d9dbd6b21356`  
		Last Modified: Tue, 03 Jun 2025 20:13:46 GMT  
		Size: 19.3 MB (19300729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2527a9eea922b4f7067174cf1d3f3c54505909950fde01762d3424d1c3ac6dea`  
		Last Modified: Tue, 03 Jun 2025 20:13:48 GMT  
		Size: 20.1 MB (20148611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9df2848a84bce19f34f021f052bf61f935d50eced0096a2fd79b7cbf177897f`  
		Last Modified: Tue, 03 Jun 2025 20:13:47 GMT  
		Size: 796.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf6a0da4593ca0edd6f5255445d3cea7a9ccd095cff9fd20f90dce125ee795b`  
		Last Modified: Tue, 03 Jun 2025 20:13:47 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f67c3db59c3facece5ff3ffe2264fb0414249e137dc612ce7106e855cdc710`  
		Last Modified: Tue, 03 Jun 2025 20:13:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7f291f1f9bea439eeceb3ee2b646a0cd67be3b51c4b64fd58db56273b57a94`  
		Last Modified: Tue, 03 Jun 2025 20:14:18 GMT  
		Size: 246.1 MB (246071824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e37eaddc74d3a7b7000b4689dad7a48d9a140519bacb70a10c3e7573be9e77`  
		Last Modified: Tue, 03 Jun 2025 20:13:51 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f42be5b46001a92d820f5b92606fed04688a450fef6690daa768fd9cf4ad719`  
		Last Modified: Tue, 03 Jun 2025 20:13:52 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:b149622649d89b512eb2e457b238992973f553dc45e116f5c88a4752977d6b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 KB (62570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159cece23774e4724611776345b545ff7390cf16d05b03a22e6b968afe4ee369`

```dockerfile
```

-	Layers:
	-	`sha256:d97aa363d18f6ff32e3570bed3af5d7b99b0309a50f28bf6e6ad22054c749d2a`  
		Last Modified: Wed, 04 Jun 2025 10:04:58 GMT  
		Size: 62.6 KB (62570 bytes)  
		MIME: application/vnd.in-toto+json
