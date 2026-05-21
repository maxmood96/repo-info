## `friendica:latest`

```console
$ docker pull friendica@sha256:4b9c2b681fac3db73a17a86b2b974e302ed5f51e1595a9303900b7145fb936fa
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

### `friendica:latest` - linux; amd64

```console
$ docker pull friendica@sha256:3aa97eec12cd2de24ae1f27f686edd750a908e167fbbb1c9503b4f450aded191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305350935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a8d761b4d337f70d841385f0109e924aa2047125dd997423ab76351fb99ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Thu, 21 May 2026 18:15:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 21 May 2026 18:15:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:15:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:17:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra         gettext     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:17:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:17:37 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:17:37 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 21 May 2026 18:17:37 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:17:37 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:17:37 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:17:37 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:17:37 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:17:37 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:17:51 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:52 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:17:52 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:17:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1139d089946116b5f5a785489fbb4d205fcabed8e866e5fe291ad0b57c6bdbb0`  
		Last Modified: Thu, 21 May 2026 18:18:01 GMT  
		Size: 20.7 MB (20671261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0906eb93152c981747bffb7e8cc59f15e15b9c251dfd5162b0d0752924972a1`  
		Last Modified: Thu, 21 May 2026 18:18:00 GMT  
		Size: 1.1 MB (1133151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a4c79fce1f50453a36504ecc91a6b5d0e64ad930bbfd09adddc6eaaa41a04`  
		Last Modified: Thu, 21 May 2026 18:18:02 GMT  
		Size: 49.1 MB (49058087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4c8c81730761f2cc10efff67dd49428e17b9e71900170f882e5f18277cfdd`  
		Last Modified: Thu, 21 May 2026 18:18:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc0aaff25b2b37063cb31db1b325dba7931644b9529aaa59fad5120b4315605`  
		Last Modified: Thu, 21 May 2026 18:18:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3276fa8d4138131ea06c9b0d495dd0a8768995130b473de5c9f6a903462a72d`  
		Last Modified: Thu, 21 May 2026 18:18:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116694eb635acca344f76545d72f456fd15827283df0f42f082d188b76a5d2b6`  
		Last Modified: Thu, 21 May 2026 18:18:04 GMT  
		Size: 58.1 MB (58143549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9612b0ff9a9224832ca31bd843683171fcf0b0b25d576a493fec690daf8cc5b`  
		Last Modified: Thu, 21 May 2026 18:18:03 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc490809b8d53628f939d956ff3cf453db922dfeffed1628bf332958f216557`  
		Last Modified: Thu, 21 May 2026 18:18:03 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:1d7ab5a3a3dcb82a0af5bdb9391c6b9fa790fb48acd2f0eafd941ce561c78de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 KB (70303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eb2eea08ea87df3aab3c557b5b0e6f1ccc51a7861fa0ffa534c9fbd35bf0cb`

```dockerfile
```

-	Layers:
	-	`sha256:8c9eeb801e2802bae178a6544bd9f6bc2dd173c9a6bc518975c877892fff58b3`  
		Last Modified: Thu, 21 May 2026 18:18:00 GMT  
		Size: 70.3 KB (70303 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; arm variant v5

```console
$ docker pull friendica@sha256:a913e70c6377e1c38f586710d7568b417ce95104c72a528ba1eae1911cbb63b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275970505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9224ea0143561abf9620cf69c5942e9979b8bfb945769f6215b94fb06da8454b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:09:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:09:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:09:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:09:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:09:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:09:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:09:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:13:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:13:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:13:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:13:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:13:42 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:13:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:17:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:17:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:17:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:17:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:17:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:17:00 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:17:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:17:01 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:17:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:17:01 GMT
CMD ["apache2-foreground"]
# Thu, 21 May 2026 18:14:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 21 May 2026 18:14:26 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:14:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:17:31 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra         gettext     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:31 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:17:31 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:17:31 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:17:31 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 21 May 2026 18:17:31 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:17:31 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:17:31 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:17:31 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:17:31 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:17:31 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:17:51 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:51 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:17:51 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:17:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:17:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94262adb83cfc442e94a7095d67f06e528abf0ba5b8f67d6aaad77d3d1719c3`  
		Last Modified: Tue, 19 May 2026 23:13:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd2f72d3a71c652360d2fba84b45d7438b9f28239b020172a261bf670bcf01c`  
		Last Modified: Tue, 19 May 2026 23:13:25 GMT  
		Size: 94.9 MB (94885954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c06e5433310da2226c66e6315a36d155244996967881157fc140023c24c2a`  
		Last Modified: Tue, 19 May 2026 23:13:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec78090d65909b48c3b8c9bb919200ec68173f3154bb22a5514866f0ff0b3fa3`  
		Last Modified: Tue, 19 May 2026 23:17:11 GMT  
		Size: 4.1 MB (4090128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9694220ad1a3a1740cbb27629c68e85d228a9d920e1f765dc86b6bf556030b`  
		Last Modified: Tue, 19 May 2026 23:17:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150c2cfd62363991f179a132141a15592ae45235d5ea723f213ebed9c0fd5fc`  
		Last Modified: Tue, 19 May 2026 23:17:11 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66512943f208cd59278246221d12d721149477839c9b6a4a89b5b09ae5e9b2c1`  
		Last Modified: Tue, 19 May 2026 23:17:12 GMT  
		Size: 12.8 MB (12767528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f99505249d9ce264831bb3684c03044d33d426634689f5783008ed0e53f927`  
		Last Modified: Tue, 19 May 2026 23:17:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12a0c3a997f07e22eb8103f402c40c9e26f25d2ecc2dd21a6f7a0aa97017c2c`  
		Last Modified: Tue, 19 May 2026 23:17:12 GMT  
		Size: 10.6 MB (10603067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8574af6a5d838d85ac9993e6ac0666d835d39d832e8383ad048ef5d8b10f5228`  
		Last Modified: Tue, 19 May 2026 23:17:13 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9533b48c327fd1249fcf08a93489e15c7bc92677d2bbff7642df0a3e5adc8f7e`  
		Last Modified: Tue, 19 May 2026 23:17:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211eb20abf73c657de49badbf19d5d557057094ab7d621e3a65a96dbf454946`  
		Last Modified: Tue, 19 May 2026 23:17:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58802fb7061758e638d42f7b0e2adb8253a9d88962088235527b08a9ed03adcc`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4768ab023ce3f156d23e4173fd5e0eaaf67991cbefe8f5107599233598a3f4b4`  
		Last Modified: Thu, 21 May 2026 18:18:02 GMT  
		Size: 20.0 MB (19996359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83c89db4311c1904b93049f88c0743faea6c987459532d89670793fd4e3bfcb`  
		Last Modified: Thu, 21 May 2026 18:18:01 GMT  
		Size: 1.1 MB (1107977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad15a02a1b0ac084b654dfb9f6098e9bf5acf2e070c0cb16dcf71440a3f18452`  
		Last Modified: Thu, 21 May 2026 18:18:04 GMT  
		Size: 46.4 MB (46413142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b0d1338d47175da58c0a1cfa537191ee4d8d2697be19980f844dfd8f697d13`  
		Last Modified: Thu, 21 May 2026 18:18:01 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c64fe6f50300485a93564ef1dfeedac02873f70cf823d2b79e795e97569f07`  
		Last Modified: Thu, 21 May 2026 18:18:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e348bd2d9c7f0b0962e94612fc4121ab48d0a4289da0a137f9ccde5e59ff7126`  
		Last Modified: Thu, 21 May 2026 18:18:03 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07aa1e31112a1048d6acff66f6c235af40f730252067ef44cc87e9d1c1bb2b77`  
		Last Modified: Thu, 21 May 2026 18:18:05 GMT  
		Size: 58.1 MB (58141345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4686cbeb9a4ae0168791755fbeff84b4d791c1783d2d0e3e7f9b95f3432258a4`  
		Last Modified: Thu, 21 May 2026 18:18:04 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe729d17015791112b68aac3bdf6a8c6fe0101df3086a3cc24e5a5c26b703d7`  
		Last Modified: Thu, 21 May 2026 18:18:04 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:95b665db0fd50957359a5cc5289f07ab976de52934c87350cef69b60a45d1787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 KB (70468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5490d19a384d912beb05ab0e17160f334a348a49db448d3187925ef5569a87`

```dockerfile
```

-	Layers:
	-	`sha256:b8a5d6ac7ea6eed8447632836cb3ded4f43b828cea77a6a2a8b6352d70391703`  
		Last Modified: Thu, 21 May 2026 18:18:01 GMT  
		Size: 70.5 KB (70468 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; arm variant v7

```console
$ docker pull friendica@sha256:1f96be950d818e07c8dec445c77e31bb4c4c70807780acb289f34725119b3198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262917813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28165ce92fd8ee0382e10c959c7bcf5311ea2283abfd06d04d4ae3b8d9bcf1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:04:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:04:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:04:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:04:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:04:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:04:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:18:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:18:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:18:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:18:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:18:00 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:18:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:20:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:20:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:20:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:20:52 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:20:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:52 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:20:52 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:20:52 GMT
CMD ["apache2-foreground"]
# Thu, 21 May 2026 18:14:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 21 May 2026 18:14:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:14:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:17:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra         gettext     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:17:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:17:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:17:40 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 21 May 2026 18:17:40 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:17:40 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:17:40 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:17:40 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:17:40 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:17:40 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:17:58 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:17:58 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:17:58 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:17:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:17:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd6801d93f0ed4cd81b7c0073ea41331904e40f15b380278a52e29a77f4979d`  
		Last Modified: Tue, 19 May 2026 23:07:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990e9f3e45447308ed251fff48366ed264ca81931e5b660bd85897bd44bd60ad`  
		Last Modified: Tue, 19 May 2026 23:07:51 GMT  
		Size: 86.3 MB (86256377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f38352a9af9e503ea7357deed4317896b9201ec7af070f32076fad639a9515`  
		Last Modified: Tue, 19 May 2026 23:07:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082cd690b2ddd82a89244bc360b693595703c34967445a93c983def19e28759b`  
		Last Modified: Tue, 19 May 2026 23:21:03 GMT  
		Size: 3.8 MB (3756733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc92dd6028824eac1065afdf3c29866734e7f543279109d3dabeda4bfcfe12d`  
		Last Modified: Tue, 19 May 2026 23:21:03 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d381e4fa200d83903b09c18631e8e677763accd39268e28765542d366bcb331e`  
		Last Modified: Tue, 19 May 2026 23:21:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbebc7b1b24e4c83de725409b2c878d380d94aec3919f64340f699ee09750c7`  
		Last Modified: Tue, 19 May 2026 23:21:03 GMT  
		Size: 12.8 MB (12767749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682829bad4ce0de58c791bc1053f2eb3f46195d844f26254e96f14952e65f097`  
		Last Modified: Tue, 19 May 2026 23:21:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9922bf33da29ad45eae9117bbf615ded8b5c2fa8ea7368d2721fcafc424f8c1`  
		Last Modified: Tue, 19 May 2026 23:21:04 GMT  
		Size: 10.1 MB (10073998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bb7c60bfc4633029fd2ecd056c37ee0adc2bf93287bdcab402a06730d90a0`  
		Last Modified: Tue, 19 May 2026 23:21:04 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f456ea6d2a2f9d8f77c9f34dedfccffcf741d623a1e6a9da5a7bb8d3b375829`  
		Last Modified: Tue, 19 May 2026 23:21:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cad248bb6b221ba9e033f2081350e00685a9d953681bb83ed579605d833862a`  
		Last Modified: Tue, 19 May 2026 23:21:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4c4293cb918079f234f8d62755bb9a17fc6f8d676373faba8825cfa07d24de`  
		Last Modified: Tue, 19 May 2026 23:21:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8755d692b5d91785337e092fb96f9ca09adf8b1b4b737931ef24306776c1075`  
		Last Modified: Thu, 21 May 2026 18:18:09 GMT  
		Size: 19.9 MB (19894169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ef30f084f307fa24e493dcf5d3b4012a8e2fc2a582310651bcbc7d832a0207`  
		Last Modified: Thu, 21 May 2026 18:18:08 GMT  
		Size: 1.1 MB (1098186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f115a46c73c59e1aa76d6668bd8dee657812c688ab17a7204167e2b8782636`  
		Last Modified: Thu, 21 May 2026 18:18:09 GMT  
		Size: 44.7 MB (44712214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049da00f70c833a8dd24ed8ac1dc4ee77191a2107c2b4b1a13f4540c84409576`  
		Last Modified: Thu, 21 May 2026 18:18:08 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f97ee0b769981d663901d21c57292020cce45947c8e4e0fb9802b92c2f93005`  
		Last Modified: Thu, 21 May 2026 18:18:09 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a028a3e0325d66987384c58dc2417ed6cb4898a3a5a9753d45bfa0171d4ba050`  
		Last Modified: Thu, 21 May 2026 18:18:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d39f3ca150103dbd0dabdd7c387c0c2d612a0c762b7b9ad29b6c8a40217aaf3`  
		Last Modified: Thu, 21 May 2026 18:18:12 GMT  
		Size: 58.1 MB (58141415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1cc8d6883ce4a475fe32ca72f816fad29dc22d917350f48a6c46ecfda2ed4b`  
		Last Modified: Thu, 21 May 2026 18:18:10 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbfa0df6c1aa4bc56b70078fbb23ac866a67218b7f7267b046d907d0acebe28`  
		Last Modified: Thu, 21 May 2026 18:18:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:18eda68e2d04e7f0aa5c00baad5cbd225d44ed9eef6ee090ab1207ee61c9299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 KB (70468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ec072bb292be5c77913267ebdee9bec9e42095b9e5ad043176116dc720d876`

```dockerfile
```

-	Layers:
	-	`sha256:88c24b8ea6b793a9844b30827224af2f971421574b572d04e3b0a9281715ebb4`  
		Last Modified: Thu, 21 May 2026 18:18:07 GMT  
		Size: 70.5 KB (70468 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:acf8b18eec9e2c088e0966af37f8e8181991f2fc672a9c92a5a7ba31d9985ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297074208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e848c87b5df53a76c80b15ea4d00e54749c8d4d8ab9c775aea90e5d13187a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:30:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 20 May 2026 00:31:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 May 2026 00:31:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 00:34:28 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:34:28 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 00:34:28 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 00:34:29 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 20 May 2026 00:34:29 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 20 May 2026 00:34:29 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 20 May 2026 00:34:29 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 00:34:29 GMT
VOLUME [/var/www/data]
# Wed, 20 May 2026 00:34:29 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 20 May 2026 00:34:29 GMT
ENV FRIENDICA_VERSION=2026.01
# Wed, 20 May 2026 00:34:29 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d985715f368e106f070519e1e30240b023f31604b3d9e4cc09f23d4d5150147d
# Wed, 20 May 2026 00:34:44 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:34:44 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 00:34:44 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 20 May 2026 00:34:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:34:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3289b2fe22e5ec22e4c18b6de93877c927104763eac7b3349bd40eeca9b8636e`  
		Last Modified: Wed, 20 May 2026 00:34:55 GMT  
		Size: 20.4 MB (20387796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de798351354c29dc0d81a6de7803419e9878d346b5e76f5baa329a12448f9384`  
		Last Modified: Wed, 20 May 2026 00:34:54 GMT  
		Size: 1.1 MB (1065058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754dd9cbf3ac429ce9e60b8b1bc34757bd0a48087554d7ec805e0ca252cf779`  
		Last Modified: Wed, 20 May 2026 00:34:56 GMT  
		Size: 48.2 MB (48205974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cd16ed0479b48f4f9e94d9c8552346f516a7cddb22e4d8e56bcc3002ec2597`  
		Last Modified: Wed, 20 May 2026 00:34:54 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0251cefbfa666d6df0bc85369bbb64a3b9f4c405020884dd4fd528c3660877ba`  
		Last Modified: Wed, 20 May 2026 00:34:55 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315efd0ff6d30e2155df00b99dee1a6aeac01bb2013e0848e5268bdcbb985012`  
		Last Modified: Wed, 20 May 2026 00:34:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1c51a768d5dcee0c8e74d1935a644dc7e7fee114d3eff8911feeb4f8b6f94`  
		Last Modified: Wed, 20 May 2026 00:34:58 GMT  
		Size: 58.3 MB (58280578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7447ae2e38447de1db72a46eccd43741dede04e8914feeb0176ebe66aefed3b`  
		Last Modified: Wed, 20 May 2026 00:34:57 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96487538892d8b7b2f17aa734adba69a2837246dde8e3b4e3a26004bedcd09c9`  
		Last Modified: Wed, 20 May 2026 00:34:57 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:00ef82c5e0dbd1bc6830071c8a0a6e912666285740d13bd66d24bfbc2c4a677b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 KB (70440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3916d78642d545b7ed79ea360f45facc5c2810c3df9330fb634cc507ffdbc8`

```dockerfile
```

-	Layers:
	-	`sha256:5208147b4e996168a6f2b17d346387e898b4906bbc9566b1c2782f73ecd912c5`  
		Last Modified: Wed, 20 May 2026 00:34:54 GMT  
		Size: 70.4 KB (70440 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; 386

```console
$ docker pull friendica@sha256:fff05073825681806cc60edfdac9d9fe16373a8f86486e814f73230653d74a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306093958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff17f3807377bb99506291534efe5bd3d5e88cb38a5b1a1bac01971018ab807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:07:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:07:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:07:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:07:01 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:07:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:07:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:10:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:10:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:10:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:10:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:10:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:10:05 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:10:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:10:06 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:10:06 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:10:06 GMT
CMD ["apache2-foreground"]
# Thu, 21 May 2026 18:12:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 21 May 2026 18:12:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:12:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:15:45 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra         gettext     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:15:45 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:15:45 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:15:45 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:15:45 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 21 May 2026 18:15:45 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:15:45 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:15:45 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:15:45 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:15:45 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:15:45 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:16:02 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:16:02 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:16:02 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:16:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:16:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d57aec3b8297de20cf9c09aeb925b5fbaef28e491bac475d76f8296f2079d34`  
		Last Modified: Tue, 19 May 2026 23:10:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9867fba1433ea6b6499ea52c88250203c4fdcf7fa9a6adf09d48c0f9e777449`  
		Last Modified: Tue, 19 May 2026 23:10:29 GMT  
		Size: 116.1 MB (116142277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4ce30e2ce2c6d861e9286c79fe147ba88c5c927abd92a505ae53ecdde4d7a8`  
		Last Modified: Tue, 19 May 2026 23:10:26 GMT  
		Size: 4.5 MB (4459164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfa8c1f335b6532573255e1c5b2a57740a8bbb8a6377cb17ee4db525744ba0`  
		Last Modified: Tue, 19 May 2026 23:10:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b73ef1e6d190831d393b7a0cd7689d5c27dcb29fa9985dbac5fa803177f42b9`  
		Last Modified: Tue, 19 May 2026 23:10:27 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b43652f9c48c412f47fb853be7b453f21566a73104d5cffcd9e90fc1d319b5c`  
		Last Modified: Tue, 19 May 2026 23:10:28 GMT  
		Size: 12.8 MB (12769086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c96b4ec2215c5edbb40c16c4f8c450fd7feaa32a152e9d5af0768742e9243d`  
		Last Modified: Tue, 19 May 2026 23:10:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f943c10363cd1d69d3d11452b36e72c6e739741bba23f71d9f90298872806`  
		Last Modified: Tue, 19 May 2026 23:10:29 GMT  
		Size: 11.9 MB (11928860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56b1aada8f0a552a3c834647930aca54140899faec782e3d6c7b7f20a83d51`  
		Last Modified: Tue, 19 May 2026 23:10:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a971d1d61fd4c54a4e1e8be4fbcb42427df40e00706d75f20c4ed5bcdf0d98b`  
		Last Modified: Tue, 19 May 2026 23:10:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352544ab1f02697938eef78678074295bb1723c318f1fdb5f0540ea25621cf3a`  
		Last Modified: Tue, 19 May 2026 23:10:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681d94f935b5791822eea48610705eecd94d0c00fb66dc70d1590928a3f59a6f`  
		Last Modified: Tue, 19 May 2026 23:10:31 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74554a348338206bd54c1f24a1e9382d1713eb3880599f8134e662707420457a`  
		Last Modified: Thu, 21 May 2026 18:16:13 GMT  
		Size: 20.9 MB (20915902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567a1b102d8d8ca5caab8b275c36d5efcb142b6fb9175dd125a002a286b897be`  
		Last Modified: Thu, 21 May 2026 18:16:12 GMT  
		Size: 1.1 MB (1107866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877ebc143929d35bb3b8ff3d9e2236f9ec2315313e4d5d2707c7ac8968e2024`  
		Last Modified: Thu, 21 May 2026 18:16:14 GMT  
		Size: 49.3 MB (49320950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cc0c1d2a8a11f947ac0feb15ddb4900e589fbcded819b84c9a32f7909a8b98`  
		Last Modified: Thu, 21 May 2026 18:16:12 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491199b60fb7d0abd05f67348e400b8dceb85c87aa2834b07b5f3172de6678b`  
		Last Modified: Thu, 21 May 2026 18:16:13 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33323c5497e1badb75b3aeb1b4b9411ea8aae26a794b22734064bd9dfa47f68d`  
		Last Modified: Thu, 21 May 2026 18:16:13 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea43a6199eca6c21f2476282692643d8bcb1abcb72aa3e091a547b5f30a290c`  
		Last Modified: Thu, 21 May 2026 18:16:16 GMT  
		Size: 58.1 MB (58143378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3431330fe51049b4c24d26fceff9f7ea7efb6a26ab64d0dea35636fef9805628`  
		Last Modified: Thu, 21 May 2026 18:16:15 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4447ae85d7d7d86bb2bb71a6c129ff05722290c9dca18c4ca290f00d08a50c`  
		Last Modified: Thu, 21 May 2026 18:16:15 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:cde7305788d3f8f47a89d8616cede873fb4d832da74ecebdbb53f9dc03c200e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 KB (70250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b7cb8d1a250640a80cdc1579a80dc2c24951313280fd2a7065533decf814bf`

```dockerfile
```

-	Layers:
	-	`sha256:107c0b4a693284c75368ed4e1e658fe05f8ec30c60472ca2699c9225069cbd00`  
		Last Modified: Thu, 21 May 2026 18:16:11 GMT  
		Size: 70.2 KB (70250 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; ppc64le

```console
$ docker pull friendica@sha256:a48ac700697d2ba50a0fedcb67f1672ea58669266c01369b5e0385d076f6eb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303674079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09326b760c110a078aef3205ad3cccd581b72594edc941663a9ba1f1556a5c9`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 20 May 2026 00:11:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 00:11:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 May 2026 00:16:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:16:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 20 May 2026 00:16:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 May 2026 00:16:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 May 2026 00:16:21 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 May 2026 00:16:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:16:21 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:16:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 May 2026 00:16:21 GMT
CMD ["apache2-foreground"]
# Thu, 21 May 2026 18:15:11 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 21 May 2026 18:15:31 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 May 2026 18:15:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 18:21:26 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra         gettext     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:21:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 21 May 2026 18:21:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 21 May 2026 18:21:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 21 May 2026 18:21:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Thu, 21 May 2026 18:21:28 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 21 May 2026 18:21:28 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 18:21:28 GMT
VOLUME [/var/www/data]
# Thu, 21 May 2026 18:21:28 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 21 May 2026 18:21:28 GMT
ENV FRIENDICA_VERSION=2026.05
# Thu, 21 May 2026 18:21:28 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=b0a1e218c4a5a30d25b8be5a66cb97a4f4f802b98e7cf3d0d34ce045b2714ab2
# Thu, 21 May 2026 18:21:58 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 18:21:59 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 21 May 2026 18:22:00 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 21 May 2026 18:22:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 May 2026 18:22:00 GMT
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
	-	`sha256:7d2d745bf0dcac744246376e95beb846be408630c6d6fd23a6c732cebc74d2d8`  
		Last Modified: Wed, 20 May 2026 00:16:44 GMT  
		Size: 12.8 MB (12769205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe4fb353164b58bc1c5f89156eb68caafc1eb7ac11c8166f06ef76488802e44`  
		Last Modified: Wed, 20 May 2026 00:16:43 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9641fa2889945e6b0e79e36e2622ed74eee658ae02a5c884feeed529f228952b`  
		Last Modified: Wed, 20 May 2026 00:16:44 GMT  
		Size: 12.1 MB (12124997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c5666881a332167aaf9ab950bd1b2076af4383951d26cada973b02fd494cbb`  
		Last Modified: Wed, 20 May 2026 00:16:43 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85f63ac4d4929ed6fca30e90a0ab909185f635193564ed2c9294894a70d088c`  
		Last Modified: Wed, 20 May 2026 00:16:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718dd4c657000e4158ed9526aed2c8f902b916620835cb0d3e74c6b61e274399`  
		Last Modified: Wed, 20 May 2026 00:16:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50166130e28f566ac6ddb91c66b6c0632c5169d90526a5a6c8ba529b55b8ee45`  
		Last Modified: Wed, 20 May 2026 00:16:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945df7cfb19c5908a8033cc97ce8e43e8bb1365091e1ed8cb97498882c156ef6`  
		Last Modified: Thu, 21 May 2026 18:22:21 GMT  
		Size: 20.8 MB (20846087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5573535ad71e56d0b888629992bb1ee7373001ca092d4a699890710b390218`  
		Last Modified: Thu, 21 May 2026 18:22:20 GMT  
		Size: 1.1 MB (1055111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d58671338e5a0c49bd624343b22428d3166a3a9c030df9887d2ce2fca3dc`  
		Last Modified: Thu, 21 May 2026 18:22:22 GMT  
		Size: 50.6 MB (50641443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0b3f7ff8d7b6c54c30d5eee5ca933a9479c20197b6af195c06115314325628`  
		Last Modified: Thu, 21 May 2026 18:22:20 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd8b765d7d5f2daca6151205d063670801f841f823cd5fa0a2aaed59df94877`  
		Last Modified: Thu, 21 May 2026 18:22:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c10f4c97c27cb331dcfc752dc6ef53533b3fca43d914d7bc6f2a44d238aae66`  
		Last Modified: Thu, 21 May 2026 18:22:22 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad042081f46d1ab65861a3ab422bfd2591d81b9c64336c9cce8ce84a9349d19`  
		Last Modified: Thu, 21 May 2026 18:22:25 GMT  
		Size: 58.1 MB (58143916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba2ca690c1cea99dac58c4ad427890cb4d1cf38d04ddce8b14316bbb5f574`  
		Last Modified: Thu, 21 May 2026 18:22:23 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c8cca245d0823f9fe90940e9046cffc2b63ae9a3559d49c02688dcf8cc3ac`  
		Last Modified: Thu, 21 May 2026 18:22:23 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:ed16f1b9f564db3f9c110a78f471ad5f7caf04cdb4e8614d55e265495b324f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 KB (70372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8a61b1aa3b0140d2430e65fb447d2331d0c03523c287af05b56328dcc2dc2d`

```dockerfile
```

-	Layers:
	-	`sha256:1040ebdb9967520e8e9c7eb1bbb629207ce00e9d35822cc7dd63677e9c3e443d`  
		Last Modified: Thu, 21 May 2026 18:22:20 GMT  
		Size: 70.4 KB (70372 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; riscv64

```console
$ docker pull friendica@sha256:f42280401db389aabcfb3eb4674cd49347ecdf2f54834fd17c3436722abb88ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338653122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdaf899dd90b7f55ce09781015a0eff923d41df7eabe97e84df6a6fd9262d9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 21:54:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 09 May 2026 23:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 09 May 2026 23:01:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 09 May 2026 23:01:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 09 May 2026 23:01:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_VERSION=8.3.31
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Sun, 10 May 2026 06:23:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 10 May 2026 06:23:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 10 May 2026 07:14:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 10 May 2026 07:14:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 10 May 2026 07:14:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 10 May 2026 07:14:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 10 May 2026 07:14:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 10 May 2026 07:14:09 GMT
STOPSIGNAL SIGWINCH
# Sun, 10 May 2026 07:14:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 10 May 2026 07:14:09 GMT
WORKDIR /var/www/html
# Sun, 10 May 2026 07:14:09 GMT
EXPOSE map[80/tcp:{}]
# Sun, 10 May 2026 07:14:09 GMT
CMD ["apache2-foreground"]
# Tue, 12 May 2026 04:27:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 12 May 2026 04:28:34 GMT
ENV GOSU_VERSION=1.17
# Tue, 12 May 2026 04:28:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 12 May 2026 04:55:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 04:55:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 May 2026 04:55:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 May 2026 04:55:19 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 12 May 2026 04:55:20 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 12 May 2026 04:55:20 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 12 May 2026 04:55:20 GMT
VOLUME [/var/www/html]
# Tue, 12 May 2026 04:55:20 GMT
VOLUME [/var/www/data]
# Tue, 12 May 2026 04:55:20 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 12 May 2026 04:55:20 GMT
ENV FRIENDICA_VERSION=2026.01
# Tue, 12 May 2026 04:55:20 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d985715f368e106f070519e1e30240b023f31604b3d9e4cc09f23d4d5150147d
# Tue, 12 May 2026 04:56:54 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 04:56:55 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 12 May 2026 04:56:55 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 12 May 2026 04:56:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 04:56:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851920f3b2b9f32390e534dcffd1a0f98fdc6aa8d5199bfd378e81a327288ff`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0821c675bc014f36787754eae800bec2700775366123fdb7b93402865c4af1`  
		Last Modified: Sat, 09 May 2026 23:00:25 GMT  
		Size: 146.6 MB (146579482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b3119d655d94203c15aecf1cc2d93402f4523740a2527b967e186d7693c42`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fef68a865e77649624e332fc135889fa3e311fd92fbd55efb9283eaf669560`  
		Last Modified: Sun, 10 May 2026 00:03:23 GMT  
		Size: 4.0 MB (4031575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b336a94a4c9567b8427e54f2733c24a8a5678559cf7b51711a20ec3f8d801d63`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b6e8491a8e810371841937507898364acf2bcba097426fe8b034aea28f887`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc6e2880eb0be7915d2dbaa81453bc2de18bc05f3b1d4166d2612c407881474`  
		Last Modified: Sun, 10 May 2026 07:17:24 GMT  
		Size: 12.8 MB (12784303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5661fb38c663cadef341781d0a42aadf8aa69fb044450c34ce645656805a6e`  
		Last Modified: Sun, 10 May 2026 07:17:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c198adb0dab9131a037bbd9703d6028c1cb6233a1443377d7ae569374479ad4`  
		Last Modified: Sun, 10 May 2026 07:17:24 GMT  
		Size: 11.3 MB (11255901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d0a78dfb6628625a73c332903e9c67453f7462b7ad0c347876bb01dd6c7e2`  
		Last Modified: Sun, 10 May 2026 07:17:20 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114c9a6c65b069728c59b0dc26a3f67f60ab534469478686ed51af95bab89ae7`  
		Last Modified: Sun, 10 May 2026 07:17:22 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec64d122bf3466fb516cec82b07302cbd4aa648dec3c9ea2cccdfea52017449`  
		Last Modified: Sun, 10 May 2026 07:17:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6bf3d13417ff252835cf491011d5db331551d766676c43ebed357b17bf55f5`  
		Last Modified: Sun, 10 May 2026 07:17:24 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ad835e736938303c6e2986d1e31b10929eab1cd3ad33f86accfd88eedd722`  
		Last Modified: Tue, 12 May 2026 04:59:19 GMT  
		Size: 20.0 MB (20040415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068c1b1af5def0dd666c4d98e7fea07b32fb242851506f36d430e7394724ebb4`  
		Last Modified: Tue, 12 May 2026 04:59:13 GMT  
		Size: 1.1 MB (1103544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9e2dde94ea650508c9bc9597bfb56ff13d26a87f4fabddbae16fbb63f3803b`  
		Last Modified: Tue, 12 May 2026 04:59:30 GMT  
		Size: 56.3 MB (56285580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d56393e6d644a06cf1c06d54157634a5a461d4e5056360671ac8b8be557c4`  
		Last Modified: Tue, 12 May 2026 04:59:12 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadcc77abec2fef968063d0b83927c22f09e1dbba0fd34941ad51baf3d8e43ac`  
		Last Modified: Tue, 12 May 2026 04:59:14 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b713bac271f3be6bd29784b050df7f285a63abb4a844a17e6bb2dbd57681584`  
		Last Modified: Tue, 12 May 2026 04:59:15 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6413b3b65f65f1ca48f66ee2128a78e480d82898b7658195724bc818132849`  
		Last Modified: Tue, 12 May 2026 04:59:32 GMT  
		Size: 58.3 MB (58280894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924072fe01b90bf1355d67111b076f58782178fa881491d01089a4254fe23de2`  
		Last Modified: Tue, 12 May 2026 04:59:17 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cb3ee99ab15e3d01e67c58e0e96ab4fb7c15dc1bb91be43d710b9ac233b4bd`  
		Last Modified: Tue, 12 May 2026 04:59:19 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:ec216f8a4828d987fa2ac51e46e1035f12a818418497c60b86d4f7265a8fe313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 KB (70289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ade1b342b59bb117d72886e31a6c848e3fedbfea61f424d1d1cb7bc262b058f`

```dockerfile
```

-	Layers:
	-	`sha256:28a263ddc7e392ea40febe208607cea407e2be822a951729c5e9e8b4ced54c98`  
		Last Modified: Tue, 12 May 2026 04:59:12 GMT  
		Size: 70.3 KB (70289 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; s390x

```console
$ docker pull friendica@sha256:a690bbf943b9d34ed8b17b8d0675c6829d76b153bf6bd733ff7f0e307622c883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278480800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf7dbe3bba3449cb028ebb6053c26fe9c544495b57cb1b2a29deac3c6e34105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:04:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:04:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:04:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:04:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:04:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:04:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:04:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:04:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:04:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:04:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:04:22 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:25:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:25:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:28:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:28:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:28:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:28:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:28:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:28:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:28:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:28:17 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:28:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:28:17 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 02:15:06 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 20 May 2026 02:15:15 GMT
ENV GOSU_VERSION=1.17
# Wed, 20 May 2026 02:15:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 02:17:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.28;     pecl install memcached-3.4.0;     pecl install redis-6.3.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.1;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:17:46 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 02:17:46 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 02:17:46 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 20 May 2026 02:17:46 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 20 May 2026 02:17:46 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 20 May 2026 02:17:46 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 02:17:46 GMT
VOLUME [/var/www/data]
# Wed, 20 May 2026 02:17:46 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 20 May 2026 02:17:46 GMT
ENV FRIENDICA_VERSION=2026.01
# Wed, 20 May 2026 02:17:46 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=d985715f368e106f070519e1e30240b023f31604b3d9e4cc09f23d4d5150147d
# Wed, 20 May 2026 02:18:00 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz friendica-all-in-one-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-all-in-one-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:18:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 02:18:01 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 20 May 2026 02:18:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 02:18:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7295ca603439dd71b068eda2edc98538f434e45d7b546939540aca0729e13`  
		Last Modified: Tue, 19 May 2026 23:08:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddafa1a1f42da6fc100002fbf2f75fab380bfd0a0830f25002beda69712c8b6`  
		Last Modified: Tue, 19 May 2026 23:08:27 GMT  
		Size: 92.6 MB (92572865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b057ccffd567696efde4f630bd4a41cdd53adb73571f658de9efd737c20d385`  
		Last Modified: Tue, 19 May 2026 23:08:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd325e6f49d7995fec03c26393c3a22b9bbb7d8829b1bdecb57781155ab98c48`  
		Last Modified: Tue, 19 May 2026 23:08:26 GMT  
		Size: 4.3 MB (4331393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d60e2fc7acd696cd5b59ec914a4d6dcafaf88dd35816c3f2dfcfe8bce2e933d`  
		Last Modified: Tue, 19 May 2026 23:08:26 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f90e0e0d6af38a9996c22a37a96e42aab103e43be019602bca182f6d04ba7`  
		Last Modified: Tue, 19 May 2026 23:08:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72593f95af61c50a61968b0956ea9f4b59f28f5ce0775d8a33b56fd71047608f`  
		Last Modified: Tue, 19 May 2026 23:28:36 GMT  
		Size: 12.8 MB (12768450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add723036cac523c65f694f3a3c72955c073dd74fb35fb4a97200c4fb7e6bf6`  
		Last Modified: Tue, 19 May 2026 23:28:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f8a96eeeb95867bcc7ffb2e0a3fcbe84ed0657e200bffcb207571fe9587f6e`  
		Last Modified: Tue, 19 May 2026 23:28:36 GMT  
		Size: 11.6 MB (11573136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253be52f4393c263498f6c0c6813a273621f2a990281d59ed6f7c796f150b81b`  
		Last Modified: Tue, 19 May 2026 23:28:35 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d35c141966313b90c4ce3473bf18ab0d7114e51a4224e9d676e95215719804e`  
		Last Modified: Tue, 19 May 2026 23:28:36 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28853844cc031c0304cee00c461efdf78280648cc1901b86ab227566a184d4be`  
		Last Modified: Tue, 19 May 2026 23:28:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff1323d4548650c11a666919b09575722c7538f1a06ffc282bb5951d1b3c5c8`  
		Last Modified: Tue, 19 May 2026 23:28:37 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37fac9b3bcf5ebcb88164fccb4c211dbbe82e25bf39826e0d8be96359796b0`  
		Last Modified: Wed, 20 May 2026 02:18:08 GMT  
		Size: 19.9 MB (19917772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe7fb141d2cecaf78db9ffff03a1248dded34a85cb2526c8a28c974251152e`  
		Last Modified: Wed, 20 May 2026 02:18:07 GMT  
		Size: 1.1 MB (1097598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4c98e8e0911195fc7b2237d8b6fe2d36358d69c723aaf2a52a9d055fbbeb7b`  
		Last Modified: Wed, 20 May 2026 02:18:15 GMT  
		Size: 48.1 MB (48084490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2141a1de51761a1ebb7dfbc1fa21079bf04c39604092be1433ebaae50c02bc8`  
		Last Modified: Wed, 20 May 2026 02:18:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f615a3a43347a564ec1432ac0f0a5501b0562ea313a64af115ed2102a61c732c`  
		Last Modified: Wed, 20 May 2026 02:18:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b187e9cde35bf70bf9b4315e1bcb7488a9f26f290a45145daa014552c67e8263`  
		Last Modified: Wed, 20 May 2026 02:18:14 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee53d7ed56a1dc9aae9f2952f3719efcf1b7158f51dbdc6b2989a0b72249cc`  
		Last Modified: Wed, 20 May 2026 02:18:16 GMT  
		Size: 58.3 MB (58278023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59794dbf403c4c88c5dd8e62bf8e642f51897f975a9fb640993feda5a41ff1`  
		Last Modified: Wed, 20 May 2026 02:18:15 GMT  
		Size: 3.2 KB (3163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab52c4522b0648e4c62a3d533317f3ed4d237eef70c85de0381517a8dc4a0a8`  
		Last Modified: Wed, 20 May 2026 02:18:15 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:a74b12b4423c0ba4d7c66078e949c6bce97d1af71a7100900384a9707d0985a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 KB (70212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5d60b3a6ff65d94d706b0910e9153b5b700ec0aaae6c26c30b0109388bb739`

```dockerfile
```

-	Layers:
	-	`sha256:a03632e2bca64e13018f1fda0dc7ecbfe98e32e3ae4cd8bbda29d259b785e70c`  
		Last Modified: Wed, 20 May 2026 02:18:14 GMT  
		Size: 70.2 KB (70212 bytes)  
		MIME: application/vnd.in-toto+json
