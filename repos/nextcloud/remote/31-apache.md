## `nextcloud:31-apache`

```console
$ docker pull nextcloud@sha256:e775d46d9888d87d11c76bd8c5d19561e99e6975052c4c5bd7f2610392b0cbc7
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

### `nextcloud:31-apache` - linux; amd64

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

### `nextcloud:31-apache` - unknown; unknown

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

### `nextcloud:31-apache` - linux; arm variant v5

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

### `nextcloud:31-apache` - unknown; unknown

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

### `nextcloud:31-apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:e8d45a44d141b2443c342be6b529f6eaab9b90678d6b34e78108b635e7880c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.8 MB (424833266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b02a53fe19896baac2df9c45f75999bc2c51442d2a895dae85b4d050c38505`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
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
	-	`sha256:a37ff4f5b55428ab56b429909bd27f22d763e1e981463717b52e325a93fa76e9`  
		Last Modified: Fri, 06 Jun 2025 18:49:38 GMT  
		Size: 12.7 MB (12681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ac9f9b173f65e7d36f27d7da7edcb2de2a2ffbb1a35d649aaf401319fb3358`  
		Last Modified: Fri, 06 Jun 2025 18:49:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd57d28b2dc46d543c91f9dcd595a7d049af749faa6aeb924b294826aea3cd3a`  
		Last Modified: Fri, 06 Jun 2025 18:49:39 GMT  
		Size: 10.1 MB (10052900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de74c40f84b80e86031e8ad63ce5f0b1973d37cc53054e911c510a05f33a828a`  
		Last Modified: Fri, 06 Jun 2025 18:49:37 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c46cb44e5cab2f8035e3ef3808535ad347b55eccffff70db23e6cccdb682fca`  
		Last Modified: Fri, 06 Jun 2025 18:49:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bd19f9124c90fd5b360eb3bb5d9ad0c55bc1a722388c1dd80ec43d652644e2`  
		Last Modified: Fri, 06 Jun 2025 18:49:30 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebede2f33699cc2e64758139adf9a7305b20e53035046acbde73c94d22894d8d`  
		Last Modified: Fri, 06 Jun 2025 20:17:42 GMT  
		Size: 18.1 MB (18146017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5c299576b893595e534a3e49a63b85368789a6bde9339573828e4eb8a5335f`  
		Last Modified: Fri, 06 Jun 2025 20:17:44 GMT  
		Size: 18.9 MB (18943289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883ec80e4f9e14aa51443ef4e619a8e54f358e8758bbb2a7965bb3fbd5ac0d8`  
		Last Modified: Fri, 06 Jun 2025 20:17:44 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58889b4bd9f9bf116c972b5e8d6b1e40b3080565a3a1fdb2cc49290e09f00b`  
		Last Modified: Fri, 06 Jun 2025 20:17:46 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9798aac877e41e26facb49a0a3f7f0880996b2fec42f3afdc98f411d172207`  
		Last Modified: Fri, 06 Jun 2025 20:17:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3bdbe0bafe1456a6b583f7048936fe5c5c70a28a142f04655b6d9f8c23cf20`  
		Last Modified: Fri, 06 Jun 2025 23:00:43 GMT  
		Size: 246.1 MB (246072402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c39d85b8937875e4998652231126b55811a83f92cee51124a30af2d01bd67e`  
		Last Modified: Fri, 06 Jun 2025 22:08:52 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944d94098adb62de14ef41859bf52d83c3df14cc363e620998f2d57451190e4`  
		Last Modified: Fri, 06 Jun 2025 22:08:58 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:73d7cfcaffdb0819a01e1bc5b33fa6a10bf2db17aa5580bd844e064805bb450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a1b1a2b66aab0ad133aa7d801cf534746fd88905a099531314729b244169bf`

```dockerfile
```

-	Layers:
	-	`sha256:d4093ca813857cbee81f315887b741a00cc3bdade93a1d4aef18d7187e210184`  
		Last Modified: Fri, 06 Jun 2025 23:51:11 GMT  
		Size: 62.8 KB (62776 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:574bc7440012d9842d51fe503c8b582fe4894ab4f2f385cc2ad70eda8383e5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.1 MB (458085942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b261106793d37470eb1f995f54ba52d35750eadd12f0afd3724a0e7a8eac586d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3816aa6a4a22453048b3ca5b5d9565d4629dbf975474b75144dcb1402556868f`  
		Last Modified: Fri, 06 Jun 2025 17:43:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0208198dc98e848c0fc3b5ece9e85e58177daff1db54cd603e00feb8a5f0b12`  
		Last Modified: Fri, 06 Jun 2025 17:43:45 GMT  
		Size: 98.1 MB (98128225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d33d6621d222a64230b99aa02dc6f71357d7c886d060c19fe40507b14e5d84a`  
		Last Modified: Fri, 06 Jun 2025 17:43:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b028e18623f77a1007c2085c7f2bc099a65d98902b2b005d4f0255f1884ff0db`  
		Last Modified: Fri, 06 Jun 2025 17:47:13 GMT  
		Size: 20.1 MB (20121069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc7ced5a1955ee33dcf2760d3fc09fadd0815fcb36d52909f62a41048479ee`  
		Last Modified: Fri, 06 Jun 2025 17:47:10 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dedc41de90e533019610988a2917e81430917f9ddff3009bf91c93db86b815`  
		Last Modified: Fri, 06 Jun 2025 17:47:11 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2017d2d448bd75beda34731dd466c7613c65d9a5603686195b80656268fb7793`  
		Last Modified: Fri, 06 Jun 2025 18:37:58 GMT  
		Size: 12.7 MB (12683457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8196fe68cb2e41ff6dff1ba38f78a35eaf652f50fa7f1506216427dd9e2b54e`  
		Last Modified: Fri, 06 Jun 2025 18:37:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca912dab7d305f0b387b8ab14668ca0be7a92168f877c2430b094dbb2b59ff1`  
		Last Modified: Fri, 06 Jun 2025 18:38:08 GMT  
		Size: 11.7 MB (11679970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4e8356fe616efd31ef79b3d10ccbc108a9ca714d84d8a78a96e5edc3efb07e`  
		Last Modified: Fri, 06 Jun 2025 18:37:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0175ebe7e4d5413c2ae86fcc93c99eddc3ae2d0234f416f89e2388216e01976c`  
		Last Modified: Fri, 06 Jun 2025 18:37:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610ef0c8f4e8d4cb533b17851e6081c28ec8fe139a63de7fdb80ebd68bbdc3fb`  
		Last Modified: Fri, 06 Jun 2025 18:37:57 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5893ed9873a7befb2a0bb4b096b02a98843b40795f3e4800ee27801fcbbe3b97`  
		Last Modified: Fri, 06 Jun 2025 20:51:38 GMT  
		Size: 20.1 MB (20144979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802992cd956a43d5271f03957a4a90ab4c84d8d9a626aa2f25beeff79ded7646`  
		Last Modified: Fri, 06 Jun 2025 20:51:38 GMT  
		Size: 21.2 MB (21174959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcfcca6e55df018ef5a2eb2709e8d984fe3bec072140bfb94f4cedb75810272`  
		Last Modified: Fri, 06 Jun 2025 20:51:37 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ae43cfc11f1e682c9bc18983abc354203c77c65a9dcb6f986f9ef9b4098ec`  
		Last Modified: Fri, 06 Jun 2025 20:51:37 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04794479cc6740a509f51e00d73ff9734b21ef55cb9ddf17dd2799c21c734678`  
		Last Modified: Fri, 06 Jun 2025 20:51:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49724b8c267c61c2fe3e28f63aa4d4ca87acec253c5831fe80f5406d3f04ac6`  
		Last Modified: Fri, 06 Jun 2025 21:12:34 GMT  
		Size: 246.1 MB (246074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790224477f6b9a2ce29b99d3ed1f9abf58a3bd9668a002b9647c52074aa6948`  
		Last Modified: Fri, 06 Jun 2025 20:51:39 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31abb58bbc726fbf97d2b12355058af8c18e46fc52db443534a4e894655d5330`  
		Last Modified: Fri, 06 Jun 2025 20:51:39 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:52742442a8f3fa23a3b10f5d88f94b8001db27ec00ef24e775f8853fa04738fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 KB (62846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b90f37c1ba0afb90ddff2f0f8f23a1adf8edee9e3276b83b55ed683217ebd0c`

```dockerfile
```

-	Layers:
	-	`sha256:138927bcc6d8e2c35c8023240f4717caedef79ad7abc7a9af45038e89ef11b77`  
		Last Modified: Fri, 06 Jun 2025 23:51:15 GMT  
		Size: 62.8 KB (62846 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-apache` - linux; 386

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

### `nextcloud:31-apache` - unknown; unknown

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

### `nextcloud:31-apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:b33931dca393fad5045820cfdaf4b8a4a06b8ebd0b789d6fe627477c72dd16f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.3 MB (439284335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b2efa9bc2b338ac7ca39ba32294bb4e4fa4fde86156d612c77df6f0790cfca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:d5adecb421e369dbbe117a4d4dfc932ec80af54e4fea683f124c833e24c8147f`  
		Last Modified: Fri, 06 Jun 2025 19:24:22 GMT  
		Size: 12.7 MB (12681503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961eb9a0487753ade0d4684316e5d9dcfa313adf16e0def626bfdb55c972c7a2`  
		Last Modified: Fri, 06 Jun 2025 19:24:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcfe2a621605f44fba8727a639892c5676d861fbc6d9a8560001925d04508a8`  
		Last Modified: Fri, 06 Jun 2025 19:24:24 GMT  
		Size: 10.7 MB (10728080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a1baeec670d177e76f4631dfa5c923fa5bf48282096e04ee69c2f01d68d5a`  
		Last Modified: Fri, 06 Jun 2025 19:24:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b829674111d8a80dbe5c8218ef9b6e085744feb2814c0f3225a3c1f2302e1b`  
		Last Modified: Fri, 06 Jun 2025 19:24:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a3060b692987a44debfc3220e4a7a722cc9da8ec420db1f22230dd0715d42`  
		Last Modified: Fri, 06 Jun 2025 19:24:25 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bd259a8f7a6ceaebc44c079bfec66679b62757ac760fa4af105b5b0fb5193a`  
		Last Modified: Fri, 06 Jun 2025 22:59:44 GMT  
		Size: 19.8 MB (19804358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398da4ff6ef25d36f98844f1f1f41288a06721ccc360c1beeeb38ee94f28f343`  
		Last Modified: Fri, 06 Jun 2025 22:59:43 GMT  
		Size: 20.7 MB (20731377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087e28ea54904f8d11149b8e592f451364479d23a74b3613738c0963c04f666`  
		Last Modified: Fri, 06 Jun 2025 22:59:44 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358a3f762eb29cfe8c8de8c1aac8bc8b8fe89053e5a628b3a234e5141f91173a`  
		Last Modified: Fri, 06 Jun 2025 22:59:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8fd7a0de1e1589cd5b0900065fd32207ec5da878c0164b9f8dbf14cb089985`  
		Last Modified: Fri, 06 Jun 2025 22:59:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495d313f5c15ad81f7e1b5605eb7baae7b24077a63c56991f82ff681d3ef9b04`  
		Last Modified: Sat, 07 Jun 2025 02:50:38 GMT  
		Size: 246.1 MB (246073758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316e8fcef7508d16b05df5bcd3f2586aa940b880c69dadfd36a932ce813cd41b`  
		Last Modified: Fri, 06 Jun 2025 23:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c298b1594fe6b6ab35465decd12ee3e2e20a24543f1bf378e4bbf1a27116235`  
		Last Modified: Fri, 06 Jun 2025 23:26:49 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:48e9f39a825468d301d8f9dbd23bb7fdc1cb664c00e4614822237085639b465f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d3189f5db3848dbdce8b4d4e68c9a26afd1ff85901774978fe7c253e6180c4`

```dockerfile
```

-	Layers:
	-	`sha256:7477b6e0f79815b6e6c66299439a7af5797b628f330a23aef985426f6f58ed42`  
		Last Modified: Sat, 07 Jun 2025 02:50:08 GMT  
		Size: 62.7 KB (62724 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:8a28e53d59de8f1a0ce30349dd66211c292ffc5d5b0988f5d5f1438958e5a067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (472045290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78b95c694f452a27e9be2b4276fec62ce60cdbe50958364769955394912625a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:be6f0df0f1a474032cdd30fdde08ab94daea526837e2020803b99b61a49c3fd6`  
		Last Modified: Fri, 06 Jun 2025 18:24:35 GMT  
		Size: 12.7 MB (12683211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357d1d33f4f47cf35eb9d99055bb792f307d980c8036f750db1749e462d8c279`  
		Last Modified: Fri, 06 Jun 2025 18:24:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a99d939db0cf78e3a38d1c08de90a2d4406beaf5d9dcc02dd98b399cc97a5ff`  
		Last Modified: Fri, 06 Jun 2025 18:24:34 GMT  
		Size: 12.1 MB (12072505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a90e94f480192013c92869863ee0fe4b364582e59d59cf253850f3bb00e2ad`  
		Last Modified: Fri, 06 Jun 2025 18:24:33 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98c389e7a4522ef290dc8b315b31c944c28b3ddbdf4a7968b917316b9cb562a`  
		Last Modified: Fri, 06 Jun 2025 18:24:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde2346de7d5af0661ca249dc1c230d72730d968cd719c2e22deb4f60c125851`  
		Last Modified: Fri, 06 Jun 2025 18:24:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5564c23d187dead61709439cd5f689fdc6aa97098d38fb2cf6d81faf922f1ee`  
		Last Modified: Fri, 06 Jun 2025 23:51:37 GMT  
		Size: 22.6 MB (22624601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c6cab0406bbe3e31d4f3f511450d0416b69a019673580b97ad08bde1682466`  
		Last Modified: Fri, 06 Jun 2025 23:51:40 GMT  
		Size: 21.9 MB (21883131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb41449b28100aa9daefda943fb965ee578acf62881545ec3882274bcd262c6`  
		Last Modified: Fri, 06 Jun 2025 21:32:31 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653f5f1e801ab6c97e74bbe32f700b7fd20d9cb43f3304a8081b0a1a7059ef9`  
		Last Modified: Fri, 06 Jun 2025 21:32:34 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d49778e0653532b9076bb1941c109d69a3bd319b6f36c63734f5ecd122886a`  
		Last Modified: Fri, 06 Jun 2025 21:32:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37acd47ec1e2a35b5d2f440dc3280ce5f0b41437a5c45742bad56e426d35a300`  
		Last Modified: Fri, 06 Jun 2025 23:51:46 GMT  
		Size: 246.1 MB (246074242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3d0b8c1aab4c8b585d9bc2627258e58fba42119fef06c8dbbe680aa752f49a`  
		Last Modified: Fri, 06 Jun 2025 21:32:41 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d1383e1aa1614ec48a5bfa52e76f256f550d610f7a9236da0e8ed916d41f8e`  
		Last Modified: Fri, 06 Jun 2025 21:32:44 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:314f356c935d30570f0baef08fdf006067053b4d2c4cb43d832036fd401b12c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 KB (62682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f2295920bdb76c14bc0cd2f9d341725df47b5126256763dd875c207273eff4`

```dockerfile
```

-	Layers:
	-	`sha256:70327b08772031c010ad0c68c27a9866f01831e4223690fa790e90d6dc710e94`  
		Last Modified: Fri, 06 Jun 2025 23:51:22 GMT  
		Size: 62.7 KB (62682 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:ea307a4b4603bd4fd5afe5f2ed2b03f04a32bbf61af5471f12e290cafe85c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436696820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22920f1636a872df2e721eba9a874e61ae72fefb38cdbb9a9dd0e6a16ad4574`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 00:38:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:5aeba10d8f3c9020fe8c36cac9ca298353ed27dbd22e2462f6fc463d4071c5e9`  
		Last Modified: Fri, 06 Jun 2025 18:17:33 GMT  
		Size: 12.7 MB (12682122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940326f6070972f75195a9541b42a7b49a147b3a690de4bbd4aef52e29b4ece4`  
		Last Modified: Fri, 06 Jun 2025 18:17:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752d75d76324856b3b1dc49f4e7c362034906fea1cf9b99a8e6c0c84a1d15259`  
		Last Modified: Fri, 06 Jun 2025 18:17:24 GMT  
		Size: 10.9 MB (10876528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49256146fcc1d7c0eb81ba0eeb580f87aed4c12e5d6e3c68f61c26529f13fd8f`  
		Last Modified: Fri, 06 Jun 2025 18:17:23 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461345a587d2e5b43a1b353ce27c28e40668a9016497ef9f3de630b6541e7d8a`  
		Last Modified: Fri, 06 Jun 2025 18:17:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48669de194bec29f95c65f95cb260ffb0b69228668418e324573b0ef671d9df5`  
		Last Modified: Fri, 06 Jun 2025 18:17:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e2bd4d980dce8cd89a7dec7d71c762fe3bbc79fa5e7e94a6121ed598b99da6`  
		Last Modified: Fri, 06 Jun 2025 21:04:29 GMT  
		Size: 19.3 MB (19300796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e576bf286d0af619ab9f469d6da8b77487e24e40ea37663310a9a53a50259402`  
		Last Modified: Fri, 06 Jun 2025 21:04:30 GMT  
		Size: 20.1 MB (20149149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b4305bdb3e07778bfd29f6ae237cdfcc6c4d12ffc715b4294a47739cb3e847`  
		Last Modified: Fri, 06 Jun 2025 21:04:30 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44e0126018d0602ff50e64ee13acb8614c19b16ac349a8f1414e989a357461`  
		Last Modified: Fri, 06 Jun 2025 21:04:30 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d812382ede56388fa94f0b651017cfa9c2fa1d025e874dcf11ccbd0931a55e5`  
		Last Modified: Fri, 06 Jun 2025 21:04:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b123ab376c8916a0a8dc7cd56779c2954d4d8f905ae6acd195cca4525225b4`  
		Last Modified: Fri, 06 Jun 2025 23:52:14 GMT  
		Size: 246.1 MB (246071755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bcede90fcdaba065255e3e228ddb540a88de9f9487f4f1b418cdd1e9699d5f`  
		Last Modified: Fri, 06 Jun 2025 21:14:43 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb989a09b89d0d9fcff6d13d0e98caf9ee4e0c44acebc1de89a606f09f1a7d6b`  
		Last Modified: Fri, 06 Jun 2025 21:14:46 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:6400199421389ce91e59da2e490955acbcce0092633b3d8d582bbe1c5ef04c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 KB (62571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5b74844117a9729e674bee7c9c2e1414138cb6857cc626675cedfac5e97b3e`

```dockerfile
```

-	Layers:
	-	`sha256:0fc942e45a77a18aa1cce3f4d7d0062a788d2e42bf708f6e678e8e2246de3a64`  
		Last Modified: Fri, 06 Jun 2025 23:51:25 GMT  
		Size: 62.6 KB (62571 bytes)  
		MIME: application/vnd.in-toto+json
