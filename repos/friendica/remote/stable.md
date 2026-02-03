## `friendica:stable`

```console
$ docker pull friendica@sha256:f14d8848b3259e361592c2a9149f3506fc02361007246c13998ea3d0e98894dc
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

### `friendica:stable` - linux; amd64

```console
$ docker pull friendica@sha256:d5e739abdedea52d32953230c3ba64a37b0f05376d91ebde649b2748ca23646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291857361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c612da4931f3c12300d127a2fd1116838100ceb0dfdab03d2ad7bab18c6dbca6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:34:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:34:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:34:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:34:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:34:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:34:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:34:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:34:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:34:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:34:44 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:34:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:34:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:37:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:37:39 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 02:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:37:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 02:37:39 GMT
CMD ["apache2-foreground"]
# Tue, 03 Feb 2026 03:32:06 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:32:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:32:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:34:49 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:34:50 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:34:50 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 03 Feb 2026 03:34:50 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:34:50 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:34:50 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:34:50 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:34:50 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 03:34:50 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 03:34:50 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 03:34:50 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 03:35:07 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:35:07 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:35:07 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:35:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b59377e3511b7cea9cceee1f9746ea5115cd070abbb545188251527bcb5073`  
		Last Modified: Tue, 03 Feb 2026 02:37:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d3d4c99014f71b53a8dfcdcf8b91eeb32fdd2cbc0a75f0dfd4713778f1e90e`  
		Last Modified: Tue, 03 Feb 2026 02:38:04 GMT  
		Size: 104.3 MB (104334307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb1cf9d895f146c1c524fedf6b227f75c55bfff80ef4b2eb5a7c01a99384e11`  
		Last Modified: Tue, 03 Feb 2026 02:37:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01026799faa9d3a25ed4047a83dd62b604703667c0526f108bb4f9516b8c067`  
		Last Modified: Tue, 03 Feb 2026 02:38:00 GMT  
		Size: 20.1 MB (20141722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371d55d9eff5ef32355f3dd40b892e858d7b786d64f7ed63ce8797373d4a0f8c`  
		Last Modified: Tue, 03 Feb 2026 02:38:00 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c003ee756f5ec6ace0eb07be64558042b3c6ddc780f64dc21194ec77e9b47f`  
		Last Modified: Tue, 03 Feb 2026 02:38:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54df0ade03df6c2b293d360b6f12a7fc735484dd48fe3b40c0fea43132aa332f`  
		Last Modified: Tue, 03 Feb 2026 02:38:02 GMT  
		Size: 12.7 MB (12737903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c162af6a1b0363d8c0313ec5a0bf8917b035e44e8d1dae8c674784d2788873`  
		Last Modified: Tue, 03 Feb 2026 02:38:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfac9c2c532d4019e5d226b52b64681b745f1da653ca4db7a9d34b5818de61bf`  
		Last Modified: Tue, 03 Feb 2026 02:38:03 GMT  
		Size: 11.7 MB (11680359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe0fb6bb7bb9b2dd17b4febc253083ff155bc91735c545958b8cefdc73a3008`  
		Last Modified: Tue, 03 Feb 2026 02:38:03 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41ce1dc2d5f5e449990fc2079095d10b23e515437d4a048232f28ef31991fc`  
		Last Modified: Tue, 03 Feb 2026 02:38:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e854cefa77920f44f0084953f21110ba202f01b6096295377ff1d5520afc5290`  
		Last Modified: Tue, 03 Feb 2026 02:38:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbae96cd02165e26a0e7e15dbce92b18d4c22fc13425f1a0d8f4cb3e6b7b492`  
		Last Modified: Tue, 03 Feb 2026 02:38:04 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c9b8b561f4ec4104e2e7ab1b13952336516f28f984fc79127f9dfae084f284`  
		Last Modified: Tue, 03 Feb 2026 03:35:17 GMT  
		Size: 18.5 MB (18465229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b791551b51baec39137ff9c4ba1b82c56acdb1e7a879cb77205f82f2679bcaff`  
		Last Modified: Tue, 03 Feb 2026 03:35:16 GMT  
		Size: 1.1 MB (1127475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3b7b9c76696801cc2bfd69b8bfa27162e5159439115b606b9c551f1736e1ec`  
		Last Modified: Tue, 03 Feb 2026 03:35:17 GMT  
		Size: 35.5 MB (35524312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e5fcff7539f54f7b9f87c7c6edab1770049b881393276dc74680ad6db3f66`  
		Last Modified: Tue, 03 Feb 2026 03:35:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98bc1699735668cecf7e5a14f8be71b438964292df28a3582b523fb282c7e99`  
		Last Modified: Tue, 03 Feb 2026 03:35:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594d0647d08c277362ac7d7f201cac23bcf137179b2d1ce2b2b38613965ba384`  
		Last Modified: Tue, 03 Feb 2026 03:35:17 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d60b712b7f836991f17b4214d33b71a1f3b1e37c84c10dc449951d192f6027`  
		Last Modified: Tue, 03 Feb 2026 03:35:20 GMT  
		Size: 59.6 MB (59606421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f4ff0965e1d6227f3aa2ceeda99951ab0607ec665e6455eee26956ba1d6188`  
		Last Modified: Tue, 03 Feb 2026 03:35:19 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c4863a2c8554e5b6e746912a46ebe4d8393b52671ff34c32897d6e694b139`  
		Last Modified: Tue, 03 Feb 2026 03:35:19 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:aaadb05c0c000dc0bd60fd497c1fbbe2c4e269ebe056a176386582a5e8d970fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99267f34c5b2927ee828924000aa7a4b86204b8bf6e6c30872ffd741c137b28e`

```dockerfile
```

-	Layers:
	-	`sha256:1285d47530eea2157c37597571c27f58c28dc63d86f64f8f0ac9753be78e26a9`  
		Last Modified: Tue, 03 Feb 2026 03:35:16 GMT  
		Size: 72.8 KB (72765 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; arm variant v5

```console
$ docker pull friendica@sha256:1d65f9c4f48d48f0bdb88b0096372dd70f492757491791d2d5d5b67b024cfe21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261199330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f2e6da0ec6090c42ed139038b3967373a0bd3b9d73bcd5803f60f2002b4fcf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:35:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:35:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:35:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:35:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:35:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:35:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:35:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:35:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:35:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:35:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:35:32 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:45:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:48:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 02:48:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:48:22 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:48:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 02:48:22 GMT
CMD ["apache2-foreground"]
# Tue, 03 Feb 2026 04:45:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 04:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 04:45:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:48:40 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:48:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 04:48:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 04:48:40 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 04:48:40 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 03 Feb 2026 04:48:40 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 04:48:40 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 04:48:40 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 04:48:40 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 04:48:40 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 04:48:40 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 04:48:40 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 04:48:40 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 04:49:02 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:49:02 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 04:49:02 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 04:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 04:49:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e15bece2c5038698d614ed918c53e898cb82da0bcc0c7e39ead892952f2cb75`  
		Last Modified: Tue, 03 Feb 2026 02:38:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46db6bceacef7966ccb2dbbb3af0f4879cda8594969e72ef800843134e696dc`  
		Last Modified: Tue, 03 Feb 2026 02:38:50 GMT  
		Size: 82.0 MB (81983823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0bcd70d747914c95cc92e82a6a60b34784890db5ce3008b071b46b428bca5b`  
		Last Modified: Tue, 03 Feb 2026 02:38:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0969f75108e4643f6bc52ced84bf83a30d7bf01dfd193e26856436c549026f`  
		Last Modified: Tue, 03 Feb 2026 02:38:49 GMT  
		Size: 19.4 MB (19421396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44de87b167dfac7b316ff42328246796f43149628abe6133031a4fcdbcd0e2`  
		Last Modified: Tue, 03 Feb 2026 02:38:49 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f445c2d38755ad2282a0be1ca8e7e786faf1839c460c5758fc5c7faa0e1d1bd7`  
		Last Modified: Tue, 03 Feb 2026 02:38:49 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933d372c514abad2ff640d7c1a4665229a6e685383e6fee27cbb1cece37c2c0b`  
		Last Modified: Tue, 03 Feb 2026 02:48:33 GMT  
		Size: 12.7 MB (12735468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d400c9917118154ac6962d8220d262174e90c845d75fc552af9401c94612af2`  
		Last Modified: Tue, 03 Feb 2026 02:48:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdffa394382ec59ff5106f47ab0ce13584b795644a5951f6ec907f13f69dd0d`  
		Last Modified: Tue, 03 Feb 2026 02:48:33 GMT  
		Size: 10.6 MB (10617103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c47d5c3225f8ca680e9588adbbaad7f35fe221e913b20a86fd70be937d09c`  
		Last Modified: Tue, 03 Feb 2026 02:48:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4d59dc271a446fac27ce8423408f23145bd8d8ea6f2360f21544b625b2630`  
		Last Modified: Tue, 03 Feb 2026 02:48:33 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70edd5878c760442c82901298ee8fab1c04311837579ed55a345c80d41ca070`  
		Last Modified: Tue, 03 Feb 2026 02:48:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189eb068a8763a08e871a3eac3b6a5bba3cc2e1f6c520b00e0d1366a01f43d5f`  
		Last Modified: Tue, 03 Feb 2026 02:48:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba83141a4d7cc9e2fab0cf7bbbe08ef8f0c9215db943e806757060ebc77a84`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 18.2 MB (18197244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eab1236f23aab08291ce03cac79c905a682c48f69a0bc6af14e5fa1e0281b7f`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 1.1 MB (1102741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609422f3e5277a47c6709320d7b42ecae8fae6a4689ba4193a14e556fbaf9d58`  
		Last Modified: Tue, 03 Feb 2026 04:49:13 GMT  
		Size: 31.8 MB (31769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca41e0a0eff40e24f9f199adb737a7704aa9dd07c844c79c9d157ce7c140f11a`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73374c4f07109ec54dade7feae4af2fa896ca58070e7824742379ecde8ab145`  
		Last Modified: Tue, 03 Feb 2026 04:49:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501c08895d19327e50824ab54dc17ed920d6259e61a69d79a6dd6f7bc7033825`  
		Last Modified: Tue, 03 Feb 2026 04:49:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b62b6f36f18e5bbfa9338eff26becc7c27a98e0a8bdd6729a0dcf44c1c20eab`  
		Last Modified: Tue, 03 Feb 2026 04:49:16 GMT  
		Size: 59.6 MB (59603100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0a3a4aaedd535cb2ef69dc643b0cd13e40603b4a1633bbcf8db4a285be6fd`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445f934a31829179c2f303054038040c1c2fd24c552bf3926c5a354e9944ff1`  
		Last Modified: Tue, 03 Feb 2026 04:49:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:33c2dc151d753fabd615f69e893d5f19868849a18c2b2fa95e9925974ff525f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319c591ebf6377a23b5fad80cdd8a3255c47bec0cee1a1a7c4729aa36841ff6e`

```dockerfile
```

-	Layers:
	-	`sha256:fd52348ddc933a1c3fbfc93ef5a602ac77e64c7fc8293726776e026b9c060d30`  
		Last Modified: Tue, 03 Feb 2026 04:49:11 GMT  
		Size: 72.9 KB (72929 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; arm variant v7

```console
$ docker pull friendica@sha256:07fb6586d4b1221bcdd15c9e70b53a7c3d933c0c4c9bb5a4f3e2c0aceacff4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250582286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ad04fc92f84b8e6c531ce94812c83b171d80742f86a5652bb2d55cd885a4dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:36:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:37:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:37:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:37:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:37:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:37:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 Jan 2026 23:37:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 Jan 2026 23:37:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 23:37:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 Jan 2026 23:37:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:37:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:37:21 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:37:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:37:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:40:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:40:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:40:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:40:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:40:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:40:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Jan 2026 23:40:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:40:06 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:40:06 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 23:40:06 GMT
CMD ["apache2-foreground"]
# Sat, 17 Jan 2026 00:23:07 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 17 Jan 2026 00:23:16 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 00:23:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 00:25:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 00:25:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 00:25:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 00:25:54 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 00:25:54 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 17 Jan 2026 00:25:54 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 00:25:54 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:25:54 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 00:25:54 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 00:25:54 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 00:25:54 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 00:25:54 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 00:25:54 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:26:12 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 00:26:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:26:12 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:26:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7fab737c0dc1a7fec1fbaad4fad0629a37b9fca5a207267e2941554fe0d54f`  
		Last Modified: Fri, 16 Jan 2026 23:40:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8f101b39de6e8153f93d1ffe3e727cda9cf43c9794871802ca6dff938c4456`  
		Last Modified: Fri, 16 Jan 2026 23:40:24 GMT  
		Size: 76.2 MB (76151828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb90a9e1b949d38c4171099a810d8393ea32ddd482947186ebad5540e082d6`  
		Last Modified: Fri, 16 Jan 2026 23:40:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3119087f88f9a72d1e47c92da336d6c68a25516f6adf105472d3926810865cc`  
		Last Modified: Fri, 16 Jan 2026 23:40:23 GMT  
		Size: 18.9 MB (18850606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bc025269017a24288a4f494de2a1c5eb13683a333752c74cd6c8d4d246cf2`  
		Last Modified: Fri, 16 Jan 2026 23:40:23 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f656c3712326abdc7ea0726c28965dc701432500d05d64fc287bb3b866e956fd`  
		Last Modified: Fri, 16 Jan 2026 23:40:23 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fa477ee064c465dca8711578fbd6140bbb6fb5a0321a458cc9c7ed0855a682`  
		Last Modified: Fri, 16 Jan 2026 23:40:24 GMT  
		Size: 12.7 MB (12735438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d677261b6fa11317468e3e72554d51141f5a9202153ac053c70c1d880328335d`  
		Last Modified: Fri, 16 Jan 2026 23:40:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a435e83643050496148947dbdf38aeeb3a6f3661445fb0fd0ac8769f4fd86`  
		Last Modified: Fri, 16 Jan 2026 23:40:24 GMT  
		Size: 10.0 MB (10049947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5ccd14c264a1988c7034b8a2e0e63c1872c7a9dbac609ddafa9006befc140a`  
		Last Modified: Fri, 16 Jan 2026 23:40:25 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482a2b6ed1bed5790bf098f045de6bcbf93b2f0c6fbea0b6c6119ebe8d77ffd`  
		Last Modified: Fri, 16 Jan 2026 23:40:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9721f88a986173cc26e493b66c043a5a45ce269c75441cc01a2a13c8e1a6f8fe`  
		Last Modified: Fri, 16 Jan 2026 23:40:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d9fd3c3eb602ae89ec4f61c8e5a380c44ec217f6179850cba094990e95cbc9`  
		Last Modified: Fri, 16 Jan 2026 23:40:26 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea904fac63cbec98cf69a01e9aceb1726f25606a3e25f49d8b5694af2a703243`  
		Last Modified: Sat, 17 Jan 2026 00:26:22 GMT  
		Size: 18.1 MB (18097323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd78a75234e4b877924ed1f0d5eb14b503772072e480b6b058eb448af84679dc`  
		Last Modified: Sat, 17 Jan 2026 00:26:21 GMT  
		Size: 1.1 MB (1093281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bdafc979dbf7af2ebb907a2088f86664945f36fa0ad9fafb283ae8cf367978`  
		Last Modified: Sat, 17 Jan 2026 00:26:22 GMT  
		Size: 30.1 MB (30055373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc5fc9538db7704a3795f824736b734573838b5750aa749ebf4b9e05b6abc0`  
		Last Modified: Sat, 17 Jan 2026 00:26:21 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402fb8e8be39d72f69ce757aca19f881be361609fbceed7af42f01549270f9f`  
		Last Modified: Sat, 17 Jan 2026 00:26:22 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb21b96b74af7fdd2cfc13bf3553c56b29a7643e09ee2a18f2f5b115cc0a6e`  
		Last Modified: Sat, 17 Jan 2026 00:26:22 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93b6e3b609aa5e80d39e762bd74d26493887827fedf6b987e67e08af2313b2f`  
		Last Modified: Sat, 17 Jan 2026 00:26:25 GMT  
		Size: 59.6 MB (59603241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991bd9a1f2b82ff82e2ecdef6491e39ac2dbd37fe796dfe8a733a98cd12f605`  
		Last Modified: Sat, 17 Jan 2026 00:26:23 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe13236151a8dcc2075656c6b029013b98f0b63c7c5fd9e09f71070e24cb757`  
		Last Modified: Sat, 17 Jan 2026 00:26:23 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:ee7d7710389d605e238d8659cf8da464af3697c3670b4f50cc9b60bf0ee22193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5145ad9667990bd399b7ec71b2013b41eff38310ece497a2c9c65f784b3868a`

```dockerfile
```

-	Layers:
	-	`sha256:90bd34880b670aa10ce0561849c12fa87d17e5a4bbeeb2afd6c28ef8677c462a`  
		Last Modified: Sat, 17 Jan 2026 00:26:21 GMT  
		Size: 72.9 KB (72929 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:590adefdeb94cac70fe4e96d865b2172e8ce20497c0992f0b70b2dd924882bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283165179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563b7efe20167b99ae7cbb1b0335b098b41d023b6af17d655a30ca86678bf726`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:23:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:24:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:24:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:24:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:24:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:24:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:35:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:35:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:35:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:35:25 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:35:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:35:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:39:02 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 02:39:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:39:02 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:39:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 02:39:02 GMT
CMD ["apache2-foreground"]
# Tue, 03 Feb 2026 03:50:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:50:56 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:50:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:54:09 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:09 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:54:09 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:54:10 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:54:10 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:54:10 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 03:54:10 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 03:54:10 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 03:54:10 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 03:54:26 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:26 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:54:26 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:54:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87264742a4f757eff79b2ae65590ab7db4b32a34a698e15613540b99c4af1dda`  
		Last Modified: Tue, 03 Feb 2026 02:27:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6c14ef74d1387994ff431e85ba4adc5b3e13d4c7d6a50907a6483862469446`  
		Last Modified: Tue, 03 Feb 2026 02:27:40 GMT  
		Size: 98.2 MB (98166650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec213745e0dd06dccebebec5b773ed28408dd44b54dfd46e524ddfb50e0037`  
		Last Modified: Tue, 03 Feb 2026 02:27:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401191c2f674ac88ade110485aa2817d0f719cf85df779f8d500164647ed6c7`  
		Last Modified: Tue, 03 Feb 2026 02:39:15 GMT  
		Size: 20.2 MB (20163615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f536b5628ab146c463dd4d0bec17c76ebafb56ae854411fbf77abe8860fb50a`  
		Last Modified: Tue, 03 Feb 2026 02:39:14 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3327be8f08e5ac880283ccaac7d675e3168b514771f123ca45b4399d00496fc`  
		Last Modified: Tue, 03 Feb 2026 02:39:14 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cccd80f921ce94353c6c7b5bad98ff62e235e57c49fcd66e96d5ef9f6b518b`  
		Last Modified: Tue, 03 Feb 2026 02:39:15 GMT  
		Size: 12.7 MB (12737509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0de0396748d219be7567d7693777d7e700122e6bba56e87d9b917b985f865d`  
		Last Modified: Tue, 03 Feb 2026 02:39:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a0ef5385c7882a37851449ac4751e6754ffac120b3a581f9020c2d63578ca`  
		Last Modified: Tue, 03 Feb 2026 02:39:16 GMT  
		Size: 11.7 MB (11690919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab449d7af2afcf15c51815f407b56e098de94e56c2867ed238a2649d8a6d0b1c`  
		Last Modified: Tue, 03 Feb 2026 02:39:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be25b321dbaefb737f6f26c200ad10f85c9dfa4e45d8bd25a68b2b5213cd6382`  
		Last Modified: Tue, 03 Feb 2026 02:39:17 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c00f5713a3c594087fd1a3a9f7c5b5a44b712c90ee0a6991cc6b373473fcd4`  
		Last Modified: Tue, 03 Feb 2026 02:39:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0487f264eed2ed9612aaacd8eb9190177cb0c0e998ead34e99d08e0b5e15a403`  
		Last Modified: Tue, 03 Feb 2026 02:39:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea961847a59e8026c240d896b22d9022d60c42b849aa930ba034799a6fc3018f`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 18.3 MB (18254810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e90a225a8813a185ada8765244f0a058d1ff47656b3fd66b9afa19783e0f38`  
		Last Modified: Tue, 03 Feb 2026 03:54:36 GMT  
		Size: 1.1 MB (1059450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a92270beebb39d0f81729d8763bc380bd79a0c4f986a8b15483c33f7ac5168`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 33.4 MB (33367229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b0a84f20d6788b7498b66ccba0801af00253575edc63e6b9a3977e2e48e9c`  
		Last Modified: Tue, 03 Feb 2026 03:54:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d9118cb9dc9869681ee3813a7cc46b3252cf8d6015f78cbc54477f1d0b708`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab35bab5be9cb5426ad8799c6d538a70032c1f295a860afd2b9d60500d6a8583`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a2d664ba2926ebea12f5050c82c3846e7899d6a412cce2d85566c94fb3b0e6`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 59.6 MB (59606020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ffbf9ca3e4f2ce131a262103c1bfdf99a4b2bdca84d7c4ffd9f5f9401dc7b2`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fd8b6c4f7361a874a099d57ced4586c685a9b5dd24f0df78725c3fe023547`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:159ce137d650ac308f2df77503cda907791236893cb0ad2bcbea7bb5b6f65bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 KB (72973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395120b2f7103bc98c04bbc4f93f5e004a85f4a4f5df44ca81e76d68f6f2149e`

```dockerfile
```

-	Layers:
	-	`sha256:609f50bd013f406f2a023f9c78971887fd5e2f76fed72b50053313267b5f818e`  
		Last Modified: Tue, 03 Feb 2026 03:54:35 GMT  
		Size: 73.0 KB (72973 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; 386

```console
$ docker pull friendica@sha256:fc28b126ba9bde7736b8d666eb7ee2542d8a9309b59a23e0c6cb59e44a803eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290544850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c05c90e7cdbeb225a28ada8b4bd7d4aebf59cf9b810b68ba8648c9a99567cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 23:22:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:22:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:22:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:22:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:22:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 Jan 2026 23:22:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 Jan 2026 23:22:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 Jan 2026 23:22:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 Jan 2026 23:22:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:22:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_VERSION=8.3.30
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 16 Jan 2026 23:22:42 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 16 Jan 2026 23:22:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:22:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:25:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:25:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:25:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:25:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Jan 2026 23:25:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:18 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:25:18 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 Jan 2026 23:25:18 GMT
CMD ["apache2-foreground"]
# Fri, 16 Jan 2026 23:57:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 16 Jan 2026 23:57:25 GMT
ENV GOSU_VERSION=1.17
# Fri, 16 Jan 2026 23:57:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 00:00:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 00:00:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 00:00:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 00:00:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:00:07 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 00:00:07 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 00:00:07 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 00:00:07 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 00:00:07 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 00:00:07 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 00:00:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 00:00:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 00:00:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 00:00:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 00:00:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50df8f6e926ed199f1442cab456f2e03aa72e9fc5ed6eabb9d9c01176ecba09`  
		Last Modified: Fri, 16 Jan 2026 23:25:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66154424cd8b69c41236cdcbcd0bf157cc3fc13296396a05a7af9d26aa5a5933`  
		Last Modified: Fri, 16 Jan 2026 23:25:39 GMT  
		Size: 101.5 MB (101522877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4e5eaed450e6b9a1d74f0d1a14b27d8a15cb4c9a08e0cce7c012f452f9860`  
		Last Modified: Fri, 16 Jan 2026 23:25:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab856e6f3f09b6caa6426c310df050e26af8a5c96297e069a44f3cf5adde820b`  
		Last Modified: Fri, 16 Jan 2026 23:25:37 GMT  
		Size: 20.7 MB (20665501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0a736316f247ea9ffae78b3ce3e19d20a216476c0eae3cd367479afc1c414b`  
		Last Modified: Fri, 16 Jan 2026 23:25:36 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe199db34164309908cafa2b0dfc95674fd0322f6abbe61d0448037b9d8532f1`  
		Last Modified: Fri, 16 Jan 2026 23:25:37 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7685c81962e47bca2387aefbf7b1e60590ef827954e2f008df98aa0a11bce3`  
		Last Modified: Fri, 16 Jan 2026 23:25:38 GMT  
		Size: 12.7 MB (12736734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614157f6ef9c345732c905f0e1710ed850c492c0fa97b2bd9fe65a2022c63bd2`  
		Last Modified: Fri, 16 Jan 2026 23:25:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7253d66bc9e71e0486d289a679d278b691cc84980f46711111d09c7a611e82`  
		Last Modified: Fri, 16 Jan 2026 23:25:39 GMT  
		Size: 11.9 MB (11885196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af740b7d92f7bd4c46202aec1c5cbc7f83c7c5e6f76c18604c54cb568ec750cd`  
		Last Modified: Fri, 16 Jan 2026 23:25:39 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295cd8bcf512ce9f20d171bd5a93f05583355586a363e213903535601666a3d0`  
		Last Modified: Fri, 16 Jan 2026 23:25:40 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc98b0ce87b47ce826947a3f2c0e739f42825ae268144fbcd4202595615e512`  
		Last Modified: Fri, 16 Jan 2026 23:25:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618892dd69c509cb2c2888525b288c2b80e5b562898c069bcdb32af1e9b912a`  
		Last Modified: Fri, 16 Jan 2026 23:25:40 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de797ce14d8a5ca4426fa365907e9dced1f250b04142dbe5ae808bc53f9d01a0`  
		Last Modified: Sat, 17 Jan 2026 00:00:34 GMT  
		Size: 19.0 MB (18983895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171d2926b72421b9c74c7b77bb2e66d2d7e0426481bc2580a18aa888b28022f3`  
		Last Modified: Sat, 17 Jan 2026 00:00:33 GMT  
		Size: 1.1 MB (1102078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b066c17c44bfe647ca4e26d4a595442f0d2ca511cd2b78e83207765a9c9088`  
		Last Modified: Sat, 17 Jan 2026 00:00:35 GMT  
		Size: 34.8 MB (34822602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8ef3b1947eb02874bb65fedce3176b002d974142b1eeb1ad25ca24dc6e089b`  
		Last Modified: Sat, 17 Jan 2026 00:00:34 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a3ee8cb2b6d0d8621292f417c8364bd4b395fc5fe58bcd8df58686acfa37a3`  
		Last Modified: Sat, 17 Jan 2026 00:00:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcaea1d22e736989e6fbd70afee9d6dd4dfc71fc50f62e5208470fe4b958c87`  
		Last Modified: Sat, 17 Jan 2026 00:00:35 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2c856af69a639575765849bbe8826277208b39210803434c0a4eb3f1ed9a7`  
		Last Modified: Sat, 17 Jan 2026 00:00:37 GMT  
		Size: 59.6 MB (59604763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce341e8104b1498478e8e9d9f1b8f17f1243e4e55f0220fe7d681cb85be73a4`  
		Last Modified: Sat, 17 Jan 2026 00:00:36 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713df7975ddbaed80485e8aa2a38ef0be6709037a34332aabda04d874a036733`  
		Last Modified: Sat, 17 Jan 2026 00:00:38 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:9cf992bc6d3d1efa0c368e6c5a26bf8ad0eb75d8c74a53e3e0dc717e12d44320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 KB (72710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e0e6dc5baf29eb6089030efa546a5a09c7df535311f3264529a5df7f5324b0`

```dockerfile
```

-	Layers:
	-	`sha256:a2b55c0e18fe1da2d4b36c8989bc8ee807ac46d3570c62edcf09ee88a91ef26c`  
		Last Modified: Sat, 17 Jan 2026 00:00:33 GMT  
		Size: 72.7 KB (72710 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; mips64le

```console
$ docker pull friendica@sha256:06f6a88d629b0874c4a8d2e789649f02ba41d500fa0c9e2735602545c7fa283b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263703200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7a8f955758f8209b58062cf44b85ec0b6221135c971aadf3940520c7cc73b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:19:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:19:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:19:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 01:19:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jan 2026 01:40:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 13 Jan 2026 01:40:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 13 Jan 2026 01:40:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:40:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_VERSION=8.3.30
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 13 Jan 2026 01:40:56 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:49:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 17 Jan 2026 00:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 01:05:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 01:05:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 01:05:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 01:05:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 01:05:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 01:05:18 GMT
STOPSIGNAL SIGWINCH
# Sat, 17 Jan 2026 01:05:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 01:05:20 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 01:05:20 GMT
EXPOSE map[80/tcp:{}]
# Sat, 17 Jan 2026 01:05:20 GMT
CMD ["apache2-foreground"]
# Sat, 17 Jan 2026 01:40:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 17 Jan 2026 01:41:01 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 01:41:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 01:52:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 01:52:56 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 01:52:56 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 01:52:58 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 01:53:00 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 17 Jan 2026 01:53:01 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 01:53:01 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 01:53:01 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 01:53:01 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 01:53:01 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 01:53:01 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 01:53:01 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 01:53:01 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 01:54:00 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 01:54:02 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 01:54:03 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 01:54:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 01:54:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:40:54 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a51a9bfcf7cf609d0809aa35fe905b8337228e88a749e1ab55783bf9036c2f1`  
		Last Modified: Tue, 13 Jan 2026 01:38:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031cebecc9a3bf8a4330bb9afd89498969466d0b89923bfe83d8b23d200df1ad`  
		Last Modified: Tue, 13 Jan 2026 01:39:11 GMT  
		Size: 80.7 MB (80673057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d27ad6411f6e09f08f7101bc8738b0def3a7fc371dd25183cbec81d8e5129bc`  
		Last Modified: Tue, 13 Jan 2026 01:38:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41cead3da08c2b729f89b8e4baff3a4046a1f3ef738b6231677097e468dbdd5`  
		Last Modified: Tue, 13 Jan 2026 02:00:26 GMT  
		Size: 20.1 MB (20078981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7ab6fe2e8fe15594d71fdd9c9d93b90d149df1f3fd3c4b1b47556670f69219`  
		Last Modified: Tue, 13 Jan 2026 02:00:23 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5d28c280ddd07ef0321c64f23fda3fbb614e0bfe0945922cf328cbbdf99f5`  
		Last Modified: Tue, 13 Jan 2026 02:00:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf2edafdcceb28fbc6c525c40b4a1a8b32a22870917daf741068359c5bf8cb3`  
		Last Modified: Sat, 17 Jan 2026 01:06:03 GMT  
		Size: 12.7 MB (12735172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bee903016c511743ecde66b7fa3c563455c5f227b35e35558ef6e482f77584b`  
		Last Modified: Sat, 17 Jan 2026 01:06:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304e160e1b44e9ea17e2711372e1ca925355c104b75fd8833cbf1702eee38237`  
		Last Modified: Sat, 17 Jan 2026 01:06:03 GMT  
		Size: 10.7 MB (10746814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301969f3a85d776158a8f96d699df1425a6ef97210894cddbf79173bafa29f7c`  
		Last Modified: Sat, 17 Jan 2026 01:06:01 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc45b4fc5124784e142443d4c2869e1495fd8f03af6109f7600a404d3a274ab9`  
		Last Modified: Sat, 17 Jan 2026 01:06:02 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87189a3416dbec932490b910713a34dc11f48d418ac17bb11fc8bf8788edf681`  
		Last Modified: Sat, 17 Jan 2026 01:06:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4661064198f047cd7e22d1099c993ac4f9078e27ea6e3d63effc83d61e10b0`  
		Last Modified: Sat, 17 Jan 2026 01:06:04 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462aa3a8a586835492a69e7321ce7e70953ec7a7cb95666c571a6940a5dcab34`  
		Last Modified: Sat, 17 Jan 2026 01:55:25 GMT  
		Size: 17.7 MB (17737390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b530dda4c1d52995abeb5a273f33ab04ac3be4c48831582422966cb9a0037ed`  
		Last Modified: Sat, 17 Jan 2026 01:55:21 GMT  
		Size: 1.0 MB (1012541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660933ff8d933debb5e9d2d74f041ce7cb259602120aa2d349f0ed9f6862d5f8`  
		Last Modified: Sat, 17 Jan 2026 01:55:29 GMT  
		Size: 32.6 MB (32589001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e121c3657f63b8d12d4fe45c1931c26139b90d8d6e6e2e2f8adc4f8e534e0d3`  
		Last Modified: Sat, 17 Jan 2026 01:55:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187342384a586957f0ab1aff7e4a6fbea3d569b70ff8f1a68dfdd856141b57f`  
		Last Modified: Sat, 17 Jan 2026 01:55:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb8365b8e5c5b1e19e02c7bcc60bb03fa90a1419be761e8dbdcafa3cdcca924`  
		Last Modified: Sat, 17 Jan 2026 01:55:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e38c8fb8b5785a6566afc08c60df407be8fb7e0a1896e73d8f1b0546ffab21`  
		Last Modified: Sat, 17 Jan 2026 01:55:33 GMT  
		Size: 59.6 MB (59605308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79ba5aa723fb8405cf94055ac65a52840dd6107d821239bf728d94d969a657`  
		Last Modified: Sun, 14 Dec 2025 07:11:47 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dbbbb3208104ca117f9d1bcb4f1ed617612d123174c09fc9eb2210bf3f0ccc`  
		Last Modified: Sat, 17 Jan 2026 01:55:25 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:a8fc3647eb70250669f60e28e4af1005948fdd906a5f37c1d2b3bc6111ffea76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdc03e5815de2af9fb20aeb88acca2efb74c93291913687bbae25aaa63fb212`

```dockerfile
```

-	Layers:
	-	`sha256:9d105ea5586458acee8ed8a80f24d4932308beeb6b7ca727bb98ec6399237651`  
		Last Modified: Sat, 17 Jan 2026 01:55:21 GMT  
		Size: 72.9 KB (72856 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; ppc64le

```console
$ docker pull friendica@sha256:e0fca636e38aaca7af1e28f30764c2496c629fadba595a13e4357337ed2f5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296255778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e7d93db10b88388894527918942a28331a81deb31cb3983e1d2503cedf288a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 23:27:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 23:29:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 23:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 23:29:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 23:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 23:29:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 23:29:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 14 Jan 2026 00:34:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 14 Jan 2026 00:34:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 14 Jan 2026 00:34:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jan 2026 00:34:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_VERSION=8.3.30
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 14 Jan 2026 00:34:59 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:33:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 17 Jan 2026 00:33:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:37:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 00:37:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:37:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 00:37:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 00:37:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 00:37:19 GMT
STOPSIGNAL SIGWINCH
# Sat, 17 Jan 2026 00:37:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:37:20 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 00:37:20 GMT
EXPOSE map[80/tcp:{}]
# Sat, 17 Jan 2026 00:37:20 GMT
CMD ["apache2-foreground"]
# Sat, 17 Jan 2026 06:04:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 17 Jan 2026 06:05:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 17 Jan 2026 06:05:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 17 Jan 2026 06:11:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 06:11:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 17 Jan 2026 06:11:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 17 Jan 2026 06:11:23 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 17 Jan 2026 06:11:24 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 17 Jan 2026 06:11:25 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 17 Jan 2026 06:11:25 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 06:11:25 GMT
VOLUME [/var/www/data]
# Sat, 17 Jan 2026 06:11:25 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 17 Jan 2026 06:11:25 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 17 Jan 2026 06:11:25 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 17 Jan 2026 06:11:25 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 17 Jan 2026 06:11:25 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 17 Jan 2026 06:12:07 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 06:12:07 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 17 Jan 2026 06:12:08 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 17 Jan 2026 06:12:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 17 Jan 2026 06:12:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00c9d4d1f21b6d304a55b7e116c52ef24850215b997b0a7114c53786a7900dd`  
		Last Modified: Tue, 13 Jan 2026 23:34:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b37bde8bf655d33e96bd4868142d3ae6d50517082efa680a17e47b74d623b4`  
		Last Modified: Tue, 13 Jan 2026 23:34:59 GMT  
		Size: 103.3 MB (103329187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b68a31428e2045dc30793a85499acb8c152ace336ad3f0098f98076ea7a713`  
		Last Modified: Tue, 13 Jan 2026 23:34:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59456b60760cc6488cea7e5448c5a099373cbfe50f18d6e796cb6d6a975f6f2`  
		Last Modified: Wed, 14 Jan 2026 00:41:25 GMT  
		Size: 21.3 MB (21332626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dee462960af4205a4a6035744110e5171d1f52b9e8a60e737214b3f97816da`  
		Last Modified: Wed, 14 Jan 2026 00:41:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f37344905834d778c185e7deb3e44c9fd5e74cf58dbc0c68480ad704dd9547`  
		Last Modified: Wed, 14 Jan 2026 00:41:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bad928943009326b6710412c8537bc97f6bffd7b109c4bc20eac5021786739`  
		Last Modified: Sat, 17 Jan 2026 00:37:53 GMT  
		Size: 12.7 MB (12737470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6960426c64b34e5d97645f4d8d9e81b80bab32f098ea1a7bf2bebafbb92589a`  
		Last Modified: Sat, 17 Jan 2026 00:37:52 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8e0b954818d3761fe52576d18e15bb4c4c48a432cc11507264169c02fe241`  
		Last Modified: Sat, 17 Jan 2026 00:37:53 GMT  
		Size: 12.1 MB (12091514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185b04ebb580a25eb624eeae4e2c1dfd17bfdf31e70c8857aa9808b8f7a63b1`  
		Last Modified: Sat, 17 Jan 2026 00:37:52 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbdec070067db6170d1c266312a24c2d8593bdbeaf56f60a6acf31b0744a294`  
		Last Modified: Sat, 17 Jan 2026 00:37:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c014ed62a8c60d0b1c7a23a66ca266f1b4587cf82f582d85e12d9bcba087ee9`  
		Last Modified: Sat, 17 Jan 2026 00:37:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591b44f55bdac5f566cf0d6e9a25ab4931d63921817927725ce91edd60d7a7f`  
		Last Modified: Sat, 17 Jan 2026 00:37:54 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60aeab4bbfbca883e5588be25588cb40fcb56b31c571534efe92c4fb6ef02bd`  
		Last Modified: Sat, 17 Jan 2026 06:12:30 GMT  
		Size: 18.6 MB (18578114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aecdb7a26821798e3d9ccc8fc1787a79a48d2ad77ca60ef6f27949752d9dfe3`  
		Last Modified: Sat, 17 Jan 2026 06:12:29 GMT  
		Size: 1.1 MB (1050767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b768652c6caa8bccf1aab79a3954fff10d6e72d6f08bf2fc774a5f630a08102c`  
		Last Modified: Sat, 17 Jan 2026 06:12:31 GMT  
		Size: 35.4 MB (35448835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6c7b6170a89a05dcb787221abc5124cad6ae0b237564fe523978b34446e31`  
		Last Modified: Sat, 17 Jan 2026 06:12:29 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d812c300b189ae6be7d7447a8eef5062555dbe4a303887cb0320a52d9cde7`  
		Last Modified: Sat, 17 Jan 2026 06:12:30 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e019921ce719e3cb2588715db688bb48d574d05ec326f793f53dd0fac931e3`  
		Last Modified: Sat, 17 Jan 2026 06:12:31 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e918d59ec343484705030ae75992c0969bb6701c5726655f958a7f0a76efaa`  
		Last Modified: Sat, 17 Jan 2026 06:12:33 GMT  
		Size: 59.6 MB (59607400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d48ce621a6c073f8221bbb206b1f0b87dc867a01cb17a8b92737fe2a3f44d`  
		Last Modified: Sat, 17 Jan 2026 06:12:32 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be9e00779c9141973902a7997a1399cc9c0d5bce25b88719dda061e421a20b`  
		Last Modified: Sat, 17 Jan 2026 06:12:32 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:52c552e24b68856d05fec2d4903412c28fc482227f76ddebc89e6e7b1cafdaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19b1ec5ed49f23043ac8bbb6aefdee89b9381cc19e904ab02516c0220c85e5e`

```dockerfile
```

-	Layers:
	-	`sha256:2d386af9722ae411de3fbf8f0c550c45c5346babbf9c671a366dcb073ad56c83`  
		Last Modified: Sat, 17 Jan 2026 06:12:28 GMT  
		Size: 72.8 KB (72833 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable` - linux; s390x

```console
$ docker pull friendica@sha256:1c72b3fa231af0076fe16ef00deb1bf6e5305888b4fd105201d7fdb4bd9c1a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261286200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e016ffeef534c0693d8c159f361a030b89ff386847d030652e3f26b562611f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:30:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:30:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:30:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:30:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:30:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:30:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:30:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:30:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:30:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:30:24 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 03:00:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 03:00:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 03:03:30 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 03:03:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 03:03:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 03:03:30 GMT
CMD ["apache2-foreground"]
# Tue, 03 Feb 2026 05:37:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 05:38:04 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 05:38:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:40:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:40:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 05:40:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 05:40:30 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 05:40:30 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 03 Feb 2026 05:40:30 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 05:40:30 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 05:40:30 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 05:40:30 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 05:40:30 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 05:40:30 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 05:40:30 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 05:40:30 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 05:40:45 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:40:45 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 05:40:45 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 05:40:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 05:40:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9655ee6b195be2bfd3d61426ce4a2830906c8dfadd7e8c4124c8b58809dbfc2f`  
		Last Modified: Tue, 03 Feb 2026 02:33:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37231254b5d72887c0519ee4b1571cc4226576086afeb5bf52d7fcd998f461b`  
		Last Modified: Tue, 03 Feb 2026 02:33:33 GMT  
		Size: 80.8 MB (80826766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79851f442186981d5b09f3f1d669553b5d06fc32279c921226a6fa5901286864`  
		Last Modified: Tue, 03 Feb 2026 02:33:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf47b768f212cef79f75df68647662b21e44a8b48d0cba8fa44a66653369689`  
		Last Modified: Tue, 03 Feb 2026 02:33:31 GMT  
		Size: 19.9 MB (19918697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d570cc82d2e4dd51560b70f7ad5056c4f14cbbd8ff7bcab976c9a803b944fa9f`  
		Last Modified: Tue, 03 Feb 2026 02:33:32 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f11dfde99a92c08dfe0125bf796d50801564862e66f295de944b5c27d3d0cb`  
		Last Modified: Tue, 03 Feb 2026 02:33:32 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6f5fe79a00dcee14929513b9c1ac0cd035c506ae12322665dcba21329e936a`  
		Last Modified: Tue, 03 Feb 2026 03:03:47 GMT  
		Size: 12.7 MB (12735775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a6e81c5f57d8126b8b774fcf8cc70f5cfc3ea9fd48a2f061aca85a8cadb73`  
		Last Modified: Tue, 03 Feb 2026 03:03:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4292870d71fe64d7e64defe3584a3f432ce2cf62625b3930bd97e53baa650d`  
		Last Modified: Tue, 03 Feb 2026 03:03:47 GMT  
		Size: 10.9 MB (10897875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2d7987923f6b4f13d25e29acc0d3c64b1322845ef3038c118e4c268aca950`  
		Last Modified: Tue, 03 Feb 2026 03:03:47 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac669aa07effd651d9feb411902eddabc540fce973efc0fa2235f4a7d6fe26c`  
		Last Modified: Tue, 03 Feb 2026 03:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa3ffb780508adedacf1da65483a750c98833afd1875f67f3993c82137777b5`  
		Last Modified: Tue, 03 Feb 2026 03:03:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443ca45fd3b7cab66424add4875f842dfbc545712307d0b3bcd665a11e77c51b`  
		Last Modified: Tue, 03 Feb 2026 03:03:48 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98eac6763b857a7897a2d99682c60cc036168d3f3436c44ed8306d6f5078dbb`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 17.7 MB (17739973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857a5eddbc751d7abfcae20ccdff47561a1b0d7b9248d6bd21cd75ee27d83c7b`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 1.1 MB (1091913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74ac3c4699f827bcf90dadaea730527b7a7f022414d52112e5b10f396e84cd9`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 31.6 MB (31576862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5633beba4b84ad8bbd1a2150474abe17d02207d4894b9010a6b0ba51ca1a7e5`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59d6bae115a4ede6e735312ce84ae7f7f117588f5ec2f270787196427fe78c`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde104133cf0faad93d1d0ed5c178bfe165fc6689fd131d6f81c3366b115b469`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af9e5266159537dcb9012ebd42a1fb45978df0f6b1f2b6d8454e7268e57823f`  
		Last Modified: Tue, 03 Feb 2026 05:41:03 GMT  
		Size: 59.6 MB (59602821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38c4399bb18b528c098a7eb07da0cf1d1d72c393748f578b81929c34956184e`  
		Last Modified: Tue, 03 Feb 2026 05:41:02 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba436c5f3c0bf4114539127f213e4d816d7979fd147289b92002dfe868ff33`  
		Last Modified: Tue, 03 Feb 2026 05:41:02 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable` - unknown; unknown

```console
$ docker pull friendica@sha256:6d63ee1fd4c28c8a74c9ebe2395d5b54d0db197a5405a7624525b90032324afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b98197c70ef572ed5374976aeb4bdbb535df596b719a0aa8348e687b6937740`

```dockerfile
```

-	Layers:
	-	`sha256:08c16f4ce385e260ff18c913dc05496682e172b2a4cfe87c83169e6d8a1cb4be`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 72.8 KB (72755 bytes)  
		MIME: application/vnd.in-toto+json
