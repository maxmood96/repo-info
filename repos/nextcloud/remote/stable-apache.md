## `nextcloud:stable-apache`

```console
$ docker pull nextcloud@sha256:9fd332ef6a4ea95b0333b79e2246d8a766acebed828cf431ebe82143bc2e22a3
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

### `nextcloud:stable-apache` - linux; amd64

```console
$ docker pull nextcloud@sha256:6effbc205b490b17c959c4fbce4a54bb6cac7fab1820f5d2c35a2e66ceff269b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.0 MB (424962861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9102cf0fc4fd474b82f4705747dfc0797f453d35f8d59ee64bfadf56dea91fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79e4c25acfd69c72bc1281aae7996225212b443e1d5ed3f0b5dc672c06eec6e`  
		Last Modified: Mon, 28 Oct 2024 22:11:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdb90068a52d99ea32b9b42687c9c110f89f70a9c7b6255a96cf006345ea0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:20 GMT  
		Size: 104.3 MB (104345039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7ce5258fc9677b44ded25c0d765c5bec2b0034a2ac37df114797fb13174ffb`  
		Last Modified: Mon, 28 Oct 2024 22:12:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3f92bad4522ccbb2c8aa28c64ee7e142e0e28a3893fa73612ce6b762dd3217`  
		Last Modified: Mon, 28 Oct 2024 22:12:17 GMT  
		Size: 20.1 MB (20123780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2e1a6860390fd2907c364c8f1fc1e8227571d12184365b52db30085d995389`  
		Last Modified: Mon, 28 Oct 2024 22:12:17 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eadf64c8bac79876e39152411e0fa242cfc43e57760af36ef9d19d30bda0eaa`  
		Last Modified: Mon, 28 Oct 2024 22:12:17 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c0c509ac913bdcc53628650e4f01881653857dd5fe09fae2efb47d9d979fac`  
		Last Modified: Mon, 28 Oct 2024 22:12:19 GMT  
		Size: 12.3 MB (12254733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f29586bcadde0b74df835b8aa209c31d4e88552de26d595c999a765e7daf6f`  
		Last Modified: Mon, 28 Oct 2024 22:12:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fe5cc5421952ff67ae87901d8bc8ff05eb6a9ecdd49fc7166fad28ec3d5936`  
		Last Modified: Mon, 28 Oct 2024 22:12:19 GMT  
		Size: 11.4 MB (11409817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d05b87f75c0e28934dc81d8157b05996c29d1767a6f59266d5fb28dc1b0116`  
		Last Modified: Mon, 28 Oct 2024 22:12:19 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0dfe201c6c3c198f24f12bee01bb27d652b7acd926146f481af045f438cd63`  
		Last Modified: Mon, 28 Oct 2024 22:12:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84359bb2faf052d4af088744f6aad85889ea993cb1694010d70604dfb4d3d12b`  
		Last Modified: Mon, 28 Oct 2024 22:12:20 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e58b8a129abdf73d847e0ddb12c23e405d539cbf3ff9d4f63620a5ddf97972`  
		Last Modified: Fri, 08 Nov 2024 22:02:45 GMT  
		Size: 22.8 MB (22784227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114adcc72b06637be219e6ea06dd33e1e2a064bb482e6261f4f9e016b46d5f06`  
		Last Modified: Fri, 08 Nov 2024 22:02:45 GMT  
		Size: 20.7 MB (20743964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7717d28b99a478b163b08ffc796ac2f66082b9b3f1994200c58e3c1a5a4c9b2`  
		Last Modified: Fri, 08 Nov 2024 22:02:44 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67d208f19f826a26388a294d4550a34ea02a1c5d52c9ea970c80ed732533125`  
		Last Modified: Fri, 08 Nov 2024 22:02:44 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9582ce2749a85996bb2da2b5e29feaeebf5982176824b00951c22721c1da7cd`  
		Last Modified: Fri, 08 Nov 2024 22:02:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01a6966380f84c57a3a648deb2bb325bee0b4f207e12e944770ddf1064ac1f1`  
		Last Modified: Fri, 08 Nov 2024 22:02:48 GMT  
		Size: 204.2 MB (204161572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e5b1f225d42e4a8b75c7a48f23fc5e08c85594f6ccc71bef2d7c4dfdfedba`  
		Last Modified: Fri, 08 Nov 2024 22:02:46 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e69596ad582c38c7555a7f1355a1f7806f65d964f9b4ac26658598bd0f4b20a`  
		Last Modified: Fri, 08 Nov 2024 22:02:46 GMT  
		Size: 2.4 KB (2398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7074fbfb5b84cbd26c1f6265e79785bfecccc29d37679d87598a43713c9cf662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 KB (60976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674c5f813a769c760e2dfebc62a47d3fc5107d9319b2a9ac51fa6e5665210419`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf0ba1f85a0d7c5771c2767a8860795e5f5839750576b94ac372314e809e1`  
		Last Modified: Fri, 08 Nov 2024 22:02:44 GMT  
		Size: 61.0 KB (60976 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:9c6c8c665a71af00d7370093d1fafa3a4a56f2fc4a443013e4ed720691cbdee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394448363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e22498300682489e88906a0a57e02bffa5deba7900e2b6d5a8a6f50072f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cbfa5cbebed9fd7c8f34077debdb42c371f3e9ff0874a76eeecaeea391fff`  
		Last Modified: Mon, 28 Oct 2024 22:06:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d7de8ee38de821e7a2d49fddb538f63c035fac91b992f00ac7bf6b39d25964`  
		Last Modified: Mon, 28 Oct 2024 22:06:33 GMT  
		Size: 82.0 MB (81993591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e85e77875bb273fe263ad3f33329ff4aec330e79ddf1f8063eaa30810787f5`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 19.4 MB (19418870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4c981efad954cf32a3908ca82953214cd6071fec1c979b34181c63546ebf8`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9718dbae37263d9bc8d722584725ce8dcc3e716cb937ff6b85801f56374c88`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c81002ebea5db38c231c4aa336151d3074b17434ccb2d96216e4320256b349`  
		Last Modified: Mon, 28 Oct 2024 22:57:48 GMT  
		Size: 12.3 MB (12253146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2adfbba0e0c8530a826bb32fff01c51e91a0c3043809909ed64723b757a757`  
		Last Modified: Mon, 28 Oct 2024 22:57:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb190b9e3894f238c93bcf4c784d32db01d3ebbb44105ee30fa4ede4073491`  
		Last Modified: Mon, 28 Oct 2024 22:57:48 GMT  
		Size: 10.4 MB (10392724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86206a8a7f986d1d2f7f9c42629b684dc15437aa76d8668a8fdbf04549f8d6b`  
		Last Modified: Mon, 28 Oct 2024 22:57:47 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc82314e6fdb9a3ccc09e9ecb08f7a5f9daa5801c12d29230eda70fbbe6ca639`  
		Last Modified: Mon, 28 Oct 2024 22:57:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7e13a42da07b0e013f2e2fd8eb58dfe943ad91b45fee2cf237ced85552092`  
		Last Modified: Mon, 28 Oct 2024 22:57:48 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9467ae44b7b1184e4176ea39bdf9f37aec524264313147437d4213811773fc3`  
		Last Modified: Tue, 29 Oct 2024 00:45:18 GMT  
		Size: 19.9 MB (19896248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2013d3a4a685f48cadd0174eb40f9863567718a11c4db9c5746a3a1fed1deb5`  
		Last Modified: Tue, 29 Oct 2024 00:45:18 GMT  
		Size: 19.4 MB (19433597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c740567d6132c6d04eafd4b6edf76632368969367bcf0a1b078008336b7fcc4e`  
		Last Modified: Tue, 29 Oct 2024 00:45:17 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1400e27d221bebee795e22ed987ee318ab1c93980033fdebc5d700457f302a5`  
		Last Modified: Tue, 29 Oct 2024 00:45:17 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eb590c9caad8ed2b1fcd9746feb5bd86a7ce1f99ad18c5c8a2e9b29c7aff17`  
		Last Modified: Tue, 29 Oct 2024 00:45:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5c7c8cc7712da81d194f40d991b36361e863be8c06f98dda81b819a8b4cd96`  
		Last Modified: Fri, 08 Nov 2024 22:11:18 GMT  
		Size: 204.2 MB (204159431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6f631e6a5a09bbc2836583a161bd9bc85a6b8e339be9c433def57fd4dcef3c`  
		Last Modified: Fri, 08 Nov 2024 22:11:11 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b79fd7b4e503f3a9f60dd02f5e4f84c40ae1a7ab14dab115af0937f66350bbb`  
		Last Modified: Fri, 08 Nov 2024 22:11:11 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:34de22fd1ac719908fa54b55a6f2b4a23e9086f40b6a3bd7d46fae2940911f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6659a52c083068d1c130dae7918be645028acfba98056c5aad8c5b399d5be7`

```dockerfile
```

-	Layers:
	-	`sha256:5d3771b5fc71fdee8518c886b3283887f27f0d399e9cb39b764680e165e242c9`  
		Last Modified: Fri, 08 Nov 2024 22:11:10 GMT  
		Size: 61.2 KB (61226 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:93ee32e72b7f0683a0d0abc2abe59162d08ac794b7bae8038da0d725f535e626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382880272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876b88f681629ffe156602ec64751619974fa8ebc219c57ec3d53bf19eca4754`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcfcb380cfbd1992d2f15637ef37999cbc4f9934874d34a17b217098fa8c2f4`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63df587ed65ffaf4f0e56a3ade450a0c2f4bd0ec52cb90e0193d9ec9a394a939`  
		Last Modified: Mon, 28 Oct 2024 22:06:06 GMT  
		Size: 76.2 MB (76163014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4e906cd29de73704abed83d01761162847c368f1a7c597dc584fd985a75c2`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42cf4a791cfd52dd382314b8b0f4cbf7a46e61d6c6c664a4299bfc5656b5a8`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 18.9 MB (18857494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf1529cc0e5c50582fc58382ef311e785b9a8a182db98e8831efef019fe199`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fca32620845d0574b19199a5b046dcb2260722f191ef3f55c582ed51287e788`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17dd877da997c8a90b113b7a3a4de0ee78417ba4b164a23a9777eef7dd204`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 12.3 MB (12253195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f43683d049b79e391e67b566556cb312d20c9370a01c10ccebd349ca230ee`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ff6f81dc6513808f18442c74f3b43791ec1b5da394df42d1324ae52fe537a`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 9.8 MB (9824909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f912b8a7b2e76994f1fc1b878024fd4b659844a75a282abca38a7ba31b39`  
		Last Modified: Tue, 29 Oct 2024 00:25:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b196057f12e508610b6fc95d578535e1364909ce3f68af288c92b405317b59b2`  
		Last Modified: Tue, 29 Oct 2024 00:25:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ced0ecd09dbb9fd88729e8c4351c27230f165445c0bebb94f5e31c3265985eb`  
		Last Modified: Tue, 29 Oct 2024 00:25:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785f73f8dcb2fe45270578b2eed65e502473a5fb5346a301940cca715f7507af`  
		Last Modified: Fri, 08 Nov 2024 22:31:41 GMT  
		Size: 18.1 MB (18135960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de83d525579a7d1c78d0c5537e46ec747b9908eb77901d702fa9f49b12b48895`  
		Last Modified: Fri, 08 Nov 2024 22:31:41 GMT  
		Size: 18.8 MB (18754597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62565653622e806bf084f9fb1127caa3760a41282fcbef8cc7c1050f5f9c7c61`  
		Last Modified: Fri, 08 Nov 2024 22:31:40 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5894aa8e1551fa203be748acd3ccbbb0be674d68a9f2b0ac5694dd0f76f6a84d`  
		Last Modified: Fri, 08 Nov 2024 22:31:40 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9812b167b6df0cfe0ed56328ebd6bec16f4b138d2c838aa9020e74132e617d`  
		Last Modified: Fri, 08 Nov 2024 22:31:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b7012a03e2ff275edb01015de01a48e50159ed33a06a77754085a7d530de5`  
		Last Modified: Fri, 08 Nov 2024 22:48:55 GMT  
		Size: 204.2 MB (204159448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d9efd7d3855ae2ed29c2715894eec3c0208596459f4bbc67bd6207eadb4dd`  
		Last Modified: Fri, 08 Nov 2024 22:48:50 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401302c8005d35f52653a2dcd421d28bd1fde9eb9d7654c9ae8fa69c50a3f43e`  
		Last Modified: Fri, 08 Nov 2024 22:48:50 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:817bd5019c4a811b809c1aac461efc838ce28ed1848cf76c4de7fa78d3a16fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee16400f4525fe32cb5013330fdc49549972a8a223883be5bda2cc45e022c3a`

```dockerfile
```

-	Layers:
	-	`sha256:59cd4f52a036b24bc51fb60742ffca790828676b98ab5de884c7a1936faa85ab`  
		Last Modified: Fri, 08 Nov 2024 22:48:49 GMT  
		Size: 61.2 KB (61217 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:cd6140264d11098662aa6bc2d18a9aed2511ba74497100f5361a6e9f740ba0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.4 MB (416367395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2136b09f2b5f496265cb36f6e30a1d11f5a049dbbcd5e01a57f7eace24485d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9b3bc8b26f6a5a92ffbc06ad21656a2707305832a76b0fa28f313b5625bfb2`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 12.3 MB (12254536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d51fa612b7c5c6cf9f22ef3eccbda3a5e594b6460e11433c9c888e2f66d1ab`  
		Last Modified: Tue, 29 Oct 2024 00:00:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799b0cdc2a8ca2df3ec16c24c1bd7ba7b3f9692f3e6ce2b22900c93b9832641`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 11.4 MB (11417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4c59e9f8a34fdcb604f7a858f3dfe169d4274ba52f5e42688893b95e3bf75f`  
		Last Modified: Tue, 29 Oct 2024 00:00:55 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73298e8100b0009502d517a801ae75e03654a75e76c0043743227ecd5a17a606`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04fb95a44d07c7a96f3ed4d463be60f41bae3da8a87e83ab65cd4c27a04f0c`  
		Last Modified: Tue, 29 Oct 2024 00:00:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5db51c617dfce6793896b70e939cdfaf8ffc4f98fbcd7592a782e5833bcd16`  
		Last Modified: Fri, 08 Nov 2024 22:58:04 GMT  
		Size: 20.1 MB (20146567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c9f3cb9b1efeb617fa54c5d5db208b510a5c83b7c1c35bae2851850cd7e4a5`  
		Last Modified: Fri, 08 Nov 2024 22:58:04 GMT  
		Size: 21.0 MB (20966727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95347459bf547d76b9aa8932966449352b2c6acb978b4d654b6417c44ef35d`  
		Last Modified: Fri, 08 Nov 2024 22:58:03 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8ec1c3835053ccf6144278e54e6a60fb967acc7e360684ebc1a00616e376d`  
		Last Modified: Fri, 08 Nov 2024 22:58:03 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181152aea0a1b7dec0ee1d8332c679167d14ad5f4d9fd6213106bdfde4bf5daf`  
		Last Modified: Fri, 08 Nov 2024 22:58:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec5c259f642a26e531e5d5c93c131b218b81118aaa43627921114563fc9defb`  
		Last Modified: Fri, 08 Nov 2024 22:58:09 GMT  
		Size: 204.2 MB (204161456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1590634f8e7175e13a5e62260928f8a0b631e61c97c62d49dcbcf141cee3bd2`  
		Last Modified: Fri, 08 Nov 2024 22:58:05 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72a1ff3477c8ea5fd0c0911ed99f575924df532d94add8ba308dc4fa194b8fa`  
		Last Modified: Fri, 08 Nov 2024 22:58:05 GMT  
		Size: 2.4 KB (2397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:f89f99101672320703c04a4acfe758b6f94cc12bfa7242e042b392c76316a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5394a6834edc5b1bd03655c00308a6a35edb14b56b9772a56b72b0c7b2c92139`

```dockerfile
```

-	Layers:
	-	`sha256:17fcea0d2eb671e7f2c944144ff764547df18df6b928edb862d32f187efb9a87`  
		Last Modified: Fri, 08 Nov 2024 22:58:02 GMT  
		Size: 61.3 KB (61296 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; 386

```console
$ docker pull nextcloud@sha256:8b09b7cf4207aa7edb7505344c991d542ab7d2d349677d975a97dd47adc4311a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423581020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a655b0a66727da23fe4f55aaf7940bcc9d498be3fb84eeafdafc2e4c1052d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f590be346b4f84fa7bcad69d1506488b3ca2c41ce3f8ec94dd6f1764c2e6b5d`  
		Last Modified: Mon, 28 Oct 2024 22:12:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbb9ce2737d52543d97d9ae1328793b53bb74d0312fc72fb8b3befa23107e0d`  
		Last Modified: Mon, 28 Oct 2024 22:12:33 GMT  
		Size: 101.5 MB (101516260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be174f186fba8bd9588e69dcb88d654cf6590053938bf88e66a215170f38003`  
		Last Modified: Mon, 28 Oct 2024 22:11:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9dc1ab6dd147e08b2d3bbe9aaa30f55305705e7c808ba69165e07ae995defc`  
		Last Modified: Mon, 28 Oct 2024 22:12:31 GMT  
		Size: 20.6 MB (20638470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150457685dc0969499bf7648934107a651cc36fd9c427add6b188d5c16406bd8`  
		Last Modified: Mon, 28 Oct 2024 22:12:30 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a956c066ccb7998aae33b550b4d7b758f9c08af75285adfaae1ee4fe9755865f`  
		Last Modified: Mon, 28 Oct 2024 22:12:31 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e66412317a10980419ce98e967721e4290be3c72b26b61c2ccef34b5cb843e`  
		Last Modified: Mon, 28 Oct 2024 22:12:33 GMT  
		Size: 12.3 MB (12254035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf58886c1e8bb7b483e5ee2d89c5e9a7e5d1ee4bf936bd0cb30a3473848ba0d`  
		Last Modified: Mon, 28 Oct 2024 22:12:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd0c35320c66e4f06cd61e442fd71ad91d9389e4e6df163cc762527bbc53e60`  
		Last Modified: Mon, 28 Oct 2024 22:12:33 GMT  
		Size: 11.6 MB (11640340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d04e1b5c03713269a72890025b7f4d77841d6969d01f94d131b28e8e5b4754`  
		Last Modified: Mon, 28 Oct 2024 22:12:33 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73b20c353711e447b05f0ac993ffc8254190663b014682a8b595144458b200e`  
		Last Modified: Mon, 28 Oct 2024 22:12:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9785ed3b33b45f262591e42e2b377625ea36dd7966219baae0dd9741cd98d0d4`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be52d4a59640085f23b3468181cadeee2725e505edf9d920497aff13194b6f11`  
		Last Modified: Fri, 08 Nov 2024 22:03:17 GMT  
		Size: 22.3 MB (22261896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52971a1913be6e7bcb9c4cefbad5d900b00f5003e86dc39990819ff053ab3688`  
		Last Modified: Fri, 08 Nov 2024 22:03:17 GMT  
		Size: 21.0 MB (20951813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a9cf0658c3986a714cc5104826aadbb635f840bdce6478886862ba9b052efe`  
		Last Modified: Fri, 08 Nov 2024 22:03:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf2f9a93cd6b7677935d49c73a1168b6019b270615399bd737856b2c7e67d9d`  
		Last Modified: Fri, 08 Nov 2024 22:03:16 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9642d2bae7dcd3fa5a6a382d12d2fb83d7aaa32f41faa4d407660a922f491`  
		Last Modified: Fri, 08 Nov 2024 22:03:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cc49e58d11b31335dca29588d84491bafa616d394b990f1f06f6f4fbac20c`  
		Last Modified: Fri, 08 Nov 2024 22:03:22 GMT  
		Size: 204.2 MB (204160520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356e35f0f3c1b6fd37ca2914182eb9ec02487c934f54fe7d11167569a3c885e6`  
		Last Modified: Fri, 08 Nov 2024 22:02:33 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967c99a6caaf14692bd8a7762b9e2178fb847259b86aec3955761e6c6376f2fb`  
		Last Modified: Fri, 08 Nov 2024 22:03:18 GMT  
		Size: 2.4 KB (2397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:04996df5ed63f1d9783f192f09dfdc0303bd77a7b61785f95165e714c965fabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 KB (60894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f01fc842ad97385132add3c3ad44da8ce87579cee3434e9bf30eece7485c8f`

```dockerfile
```

-	Layers:
	-	`sha256:b658c6be6e8d779dae3fdde2adde416302143994b96cc33241af741ef6189165`  
		Last Modified: Fri, 08 Nov 2024 22:03:16 GMT  
		Size: 60.9 KB (60894 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:73c54b0185f470bf58596e2b5061556546b8dfcbfaba5b8c6357cbc435c47948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397093696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801d0c38fd1d556caababd5697b8ad64210aa8ff5e604dc1fe573590e13f226a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75971b85139441fe144cb93dcb63eda60c20b8b82bcc4cc161a345662be6e248`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54a087649536e7da942bb23de64ede6ba55259b78328b804de7695cf731369`  
		Last Modified: Mon, 28 Oct 2024 22:20:39 GMT  
		Size: 80.7 MB (80666666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d1ae69be6bff3b5f486ce83dc2a01329491bc64c77e183361743695495d62`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805e4def2c522f97a948ff0a106d6753819d71887cabeca9b1ab8355a0ec3f5`  
		Last Modified: Mon, 28 Oct 2024 22:40:31 GMT  
		Size: 20.1 MB (20069130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f108a36b91c4b30f45222f94048f45b028abb9cbd4872f312cc17b7ebdf9e0a`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc8de30d0eaabcca7399faec8b52772f4a699389c0f6ee67d901929b205efb`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71e34b2800dfd629e12d65e7baccaaac611c653bf035588f288d647c6cb18d`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 12.3 MB (12252938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a70c912fe40d48831bad52dcdc3407fdc46c13fdfa244a823b25cb875f194ec`  
		Last Modified: Tue, 29 Oct 2024 01:00:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb0f1a43efa39a5c5633fe7071273c90673c2d33ccac2557b89a351ca8a140f`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 10.5 MB (10490881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff006eac1edc92afd7e0e7d2fa3dcb515e4b395e7aefe397576166249ea625b2`  
		Last Modified: Tue, 29 Oct 2024 01:00:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93592b97a6b773a2f914323dfd205c121226db02040b6b8d1d9bf03470ae1cb7`  
		Last Modified: Tue, 29 Oct 2024 01:00:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa01b49e578511a4a4322d6fb0a2c9f8a40ad3a1abe992b3bf142d91c31169`  
		Last Modified: Tue, 29 Oct 2024 01:00:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc343ba49ffe4626cca413d8d51d0b3b767e210aa0e5e2d7f816c0238fb23e`  
		Last Modified: Tue, 29 Oct 2024 06:40:40 GMT  
		Size: 19.8 MB (19803098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dacdf2126b1756a299784f81cbc1e7277e7408ffc9624b772343b1335a3dfa`  
		Last Modified: Tue, 29 Oct 2024 06:40:40 GMT  
		Size: 20.5 MB (20511741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6393b84fd89a18e8561234e0b9953a04dbf66dbf0e9716a0a0eaa090d795307`  
		Last Modified: Tue, 29 Oct 2024 06:40:37 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f6a118256ed408b6c02f4c30207906ec0b91193239e97e51093ff66f17cad7`  
		Last Modified: Tue, 29 Oct 2024 06:40:37 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ba3e1d3b074e02e75beaeec668e6d67d99df81db09bcea2b70231b47423f00`  
		Last Modified: Tue, 29 Oct 2024 06:40:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3375624a2ee5ff78562bb258c3948da90b713594de5fea97e5f21a74abcbada`  
		Last Modified: Fri, 08 Nov 2024 23:35:29 GMT  
		Size: 204.2 MB (204160993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34429dec017de7fda9ba22a62ae1d9ebafc1364aea25a92ed0f7286e990f1f94`  
		Last Modified: Fri, 08 Nov 2024 23:35:10 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae848ca0732a332aeb2ed64d3be526685b2acc1afefa74ede83f19e7e09001bb`  
		Last Modified: Fri, 08 Nov 2024 23:35:10 GMT  
		Size: 2.4 KB (2399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:1af1f68a0171c8a4fe27eace804001036e674b1aabc59513cdfefdbbb92f7128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08de1875e077f277fcdb75fb7fc276ddca79d297d1cdc81e7d79f51c426e523`

```dockerfile
```

-	Layers:
	-	`sha256:323eda7015438647cdf57e3b973b5aa2930f349229ca12100f401537f27fee64`  
		Last Modified: Fri, 08 Nov 2024 23:35:10 GMT  
		Size: 61.2 KB (61173 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:959319778ed12db1c5e5edfc03e72dd7ab8c5aafe15fc4438e094e57aca16539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.3 MB (430287166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765668c5183aa601c30f79da4e32c21efac8d1001f82cb41f86349f120bcb396`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae56eb39d7a6f0865b2b2c1e759158f7f32cb38431cf0b9f4a53e75069829a`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc191720824d9a8274cc0a9d7a4e17b74deb924b9ba62a638fcfe329b1cb843a`  
		Last Modified: Mon, 28 Oct 2024 22:03:58 GMT  
		Size: 103.3 MB (103321639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e65ebf34f6eed8b3368c7c37216f302c7b19e10d99d1c5ebd90d00bbf57cd63`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca7c4e1c934a05195ae2806efa08495b749078e5060a107b69954c9e8831f3`  
		Last Modified: Mon, 28 Oct 2024 22:09:18 GMT  
		Size: 21.3 MB (21308341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afeb891a5f261be3057466eac9022a1bd1afa1a3773815828cd1caeb277139c`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6afdb35491d58f7d16d1d4ace112bba4fb8ba8a1702dbad4ec8737e9e449f6`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c464ae59fd6de793ab05c94566f959b6a722b3d0e2f33eb45aed4112dd6882f6`  
		Last Modified: Mon, 28 Oct 2024 23:18:16 GMT  
		Size: 12.3 MB (12254327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef4990062e885e51b6e5e66e4af52cea186fac5d41048751518060d26b28d2`  
		Last Modified: Mon, 28 Oct 2024 23:18:15 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e936849a1a3f1ac5856040c7b30bf2cfb29e56003ba25c211c467f749b961`  
		Last Modified: Mon, 28 Oct 2024 23:18:16 GMT  
		Size: 11.8 MB (11826670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd7be0d8ea4546e014fb4b190c915ac698c4387d47e9986a555fb51e02825b3`  
		Last Modified: Mon, 28 Oct 2024 23:18:15 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f37bb6c8df119750229bc19577e1617be39f722d9174f692702d9ffd5105cfa`  
		Last Modified: Mon, 28 Oct 2024 23:18:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f093f525dd28cea67c23d9c67207443c39ff452cbbb5781cd616347bf66627`  
		Last Modified: Mon, 28 Oct 2024 23:18:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7bdabd969576a5af604fde618ee18f65e9c0add0b2992326320957ab1dcc75`  
		Last Modified: Fri, 08 Nov 2024 23:11:32 GMT  
		Size: 22.6 MB (22623327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15f3fd6416e18b476930625997fed56c66bfa5621763f1ff59fd0fcfeecab96`  
		Last Modified: Fri, 08 Nov 2024 23:11:32 GMT  
		Size: 21.7 MB (21655649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5394f3dca5d4761946ffb6748f292211b7ac8cee01800905836dd5e2dd65e`  
		Last Modified: Fri, 08 Nov 2024 23:11:31 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c963ff335a6956d07b2fec3d151446f7e254f8880d4970b80ded30fb37d447a`  
		Last Modified: Fri, 08 Nov 2024 23:11:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19423a34c959c3298931173520efd2c2ff5af17abfa64b827b223b36976e1ea6`  
		Last Modified: Fri, 08 Nov 2024 23:11:32 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8415bc5f654cb46c7efe084d2242d96148fc73ab68980ff44cfa043bf24ea4`  
		Last Modified: Fri, 08 Nov 2024 23:11:40 GMT  
		Size: 204.2 MB (204161554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a53bf291c134b45e3cdc39d935b74c548965f7aeca7ed0d88508b926cd65f`  
		Last Modified: Fri, 08 Nov 2024 23:11:33 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d357aa0ee3f49230f31fe6b7934a1e3188e9f16cbef807b2699fe681f0973e1`  
		Last Modified: Fri, 08 Nov 2024 23:11:34 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:f55c6c22d5668af634aa1dba7076a129a999db6c316af159a0027b4169ef6f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 KB (61132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf17406b81aa6886627849883042cfbc284b5742246e7362a97a0c9274868502`

```dockerfile
```

-	Layers:
	-	`sha256:26701af5863e68694fbca9e7203bb719fecd8d8ecb13f33ec4406466cefa74fb`  
		Last Modified: Fri, 08 Nov 2024 23:11:31 GMT  
		Size: 61.1 KB (61132 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable-apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:14802d1fa6fcecd8ee82c6607fac9400661a8d16e26eaf4e010463b4f34e3324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.5 MB (394525091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aac5918e138af1c6b417b02a7b820069a5f6ee87da553c53b25f1b4e78118a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 13:43:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 13:43:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_VERSION=8.2.25
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Thu, 24 Oct 2024 13:43:42 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 13:43:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 13:43:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 13:43:42 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 13:43:42 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 13:43:42 GMT
CMD ["apache2-foreground"]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
VOLUME [/var/www/html]
# Thu, 07 Nov 2024 23:24:17 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 07 Nov 2024 23:24:17 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENV NEXTCLOUD_VERSION=30.0.2
# Thu, 07 Nov 2024 23:24:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 07 Nov 2024 23:24:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Nov 2024 23:24:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef30fd559c6ef2ac6477f19c70672a7ee15e6df0955b9418d7d99e635fa1bf0`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4284cccc34f4d86bd5b1ffc10f277aa5cc0d4e8e4bf9be585b727389498bc65`  
		Last Modified: Mon, 28 Oct 2024 22:04:13 GMT  
		Size: 80.8 MB (80817298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca23539a560ecbc74c5143d2cafda70db6eb98973a13e443b451e0c9c2995f`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 19.9 MB (19895121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a45ddf6b46c9a6c7f526ae595797099a5fc579b55abcfd3898676b4d492cd2b`  
		Last Modified: Mon, 28 Oct 2024 22:09:42 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13b927d3a64cfbffb8b90c4c32f8b6e265b8d38173390a57a3b727aad43`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa275ee1b9d19202cd0025fd09bdb69741112deaa69a567fa54189ff307447b`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 12.3 MB (12253532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eb7ea1165830a1894eb7b80dc3400984fa8be48bd815fbb68abcef374a0297`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa5d847ede2e7c63d945b943316837e222c7061818e9694caeb16758c645136`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 10.6 MB (10644651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b43583c82c3ebe592c2ac63d568f1fe4184fb3a22215f28fbf712b47dd40`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d2c5d53825b9fa417d51acdf94aa5c407cb4d9c6b949ef84a3efaf9652048`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd1bc9d7872267d3f56a2b77a66e831364c5643a6e3ec078cb798eff6b35450`  
		Last Modified: Mon, 28 Oct 2024 23:59:40 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77163780760c8add2914d6cbf2bc9fe962c6a53e4737f319a684ccdad511ed83`  
		Last Modified: Fri, 08 Nov 2024 23:34:38 GMT  
		Size: 19.3 MB (19297624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99682f40c05426fa9d5e7e5ab96ec85daeea435cae9189d7a727f2ce693777f1`  
		Last Modified: Fri, 08 Nov 2024 23:34:38 GMT  
		Size: 20.0 MB (19953978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0358fa19cc5862b7e7331949f9ba82e96980229576f01c4cd2fcc510fd8be7d2`  
		Last Modified: Fri, 08 Nov 2024 23:34:38 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b51ad078db4c7027dc653062354e348828e829d1cb5e18b411a95a3150312`  
		Last Modified: Fri, 08 Nov 2024 23:34:38 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64159380b76f4352ad218591e00346494f34b21801b8f63985403a81980148e9`  
		Last Modified: Fri, 08 Nov 2024 23:34:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5bcc9a8bade4a4f15672e1f404282217e38e430ab43be7a0dbd507291f502`  
		Last Modified: Fri, 08 Nov 2024 23:34:42 GMT  
		Size: 204.2 MB (204159352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4336867099c1a69ff98496cc656fc8c202ffe9602f6d9793dc5bff3a418566f`  
		Last Modified: Fri, 08 Nov 2024 23:34:39 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85caf304f99097e2cf590b1d14329a535da3b311dde63dae0d5f95335011de19`  
		Last Modified: Fri, 08 Nov 2024 23:34:39 GMT  
		Size: 2.4 KB (2399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:fd5d1a11f0e48449042f978d56b9ef0b16eb9c1fbd9e7eddaad41bf75f0c55a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 KB (61021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025b7b06641a9ede499d24e201bc98c5bea20a2a8e72972cb262d06bff90193b`

```dockerfile
```

-	Layers:
	-	`sha256:ff43b8dea812f6e637b5d98e2ccc121990e9042b8c812cb0216c01bf20cc8734`  
		Last Modified: Fri, 08 Nov 2024 23:34:37 GMT  
		Size: 61.0 KB (61021 bytes)  
		MIME: application/vnd.in-toto+json
