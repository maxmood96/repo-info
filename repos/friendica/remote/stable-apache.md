## `friendica:stable-apache`

```console
$ docker pull friendica@sha256:0323b422a6d8d3f309b825d79d376ac1f24e605e9111b35608d0c0029e108429
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

### `friendica:stable-apache` - linux; amd64

```console
$ docker pull friendica@sha256:7f81a075d9ba1a1647c0e38a820acbb5725cd4ba794a355d04cb9e5c53431e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291828158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20f8705e7d6ec32942d274ac2b483b1aa658a7e7b9728a99f0e7795cc2d9d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:24:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:25:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:25:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:25:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:25:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:25:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:25:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:38:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:38:11 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:55:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:55:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:58:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:58:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:58:04 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:58:04 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:58:04 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jan 2026 23:30:35 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 09 Jan 2026 23:30:43 GMT
ENV GOSU_VERSION=1.17
# Fri, 09 Jan 2026 23:30:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 09 Jan 2026 23:33:05 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:33:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 09 Jan 2026 23:33:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 09 Jan 2026 23:33:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 09 Jan 2026 23:33:06 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Fri, 09 Jan 2026 23:33:06 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 09 Jan 2026 23:33:06 GMT
VOLUME [/var/www/html]
# Fri, 09 Jan 2026 23:33:06 GMT
VOLUME [/var/www/data]
# Fri, 09 Jan 2026 23:33:06 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 09 Jan 2026 23:33:06 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 09 Jan 2026 23:33:06 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 09 Jan 2026 23:33:06 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 09 Jan 2026 23:33:06 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 09 Jan 2026 23:33:22 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:33:22 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 09 Jan 2026 23:33:22 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 09 Jan 2026 23:33:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jan 2026 23:33:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963630ac40700bca53277eac42f465504ac98f81be14a88a0ecad9835241f32c`  
		Last Modified: Fri, 09 Jan 2026 22:28:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c50afb09b54e62b4d8e5a38037baad6f35c548251cf0d49306da6a94cb3ed`  
		Last Modified: Fri, 09 Jan 2026 22:28:50 GMT  
		Size: 104.3 MB (104330337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6633b600b23c0808c1efce6e7949d9ebbd0f5b0d2a199b50974357fe82f73`  
		Last Modified: Fri, 09 Jan 2026 22:28:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187d48cd69bd460ad44f92168f8e0f9265bd35f50b20536a343e6e8079470d0`  
		Last Modified: Fri, 09 Jan 2026 22:41:36 GMT  
		Size: 20.1 MB (20131837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed5042a6ff2d3d1aada0d0344194e31f0ce0a28ddb2d82e42e75d919d1db363`  
		Last Modified: Fri, 09 Jan 2026 22:41:34 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23c1e5a0c4aa79f7e93c7e42c70ef8e6795a4f55fed039fc1fd37870d510a99`  
		Last Modified: Fri, 09 Jan 2026 22:41:34 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1dcab4d4953c82e3735c5406c78ccd2f218c0a073ac41541200d5d2bc02057`  
		Last Modified: Fri, 09 Jan 2026 22:58:23 GMT  
		Size: 12.7 MB (12731090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458f18d1bb6790948e26c649b639c3d1e6bcee59547d48f4df88dadf2e776ed`  
		Last Modified: Fri, 09 Jan 2026 22:58:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653c840b869b5480526b156be8d39dde37f5eb666c9574d0246a6e6c7893cfcd`  
		Last Modified: Fri, 09 Jan 2026 22:58:24 GMT  
		Size: 11.7 MB (11677853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444a39f8bc106fb62c475b084739ca56baa5d9e8c012a753e2e59c5073a7de37`  
		Last Modified: Fri, 09 Jan 2026 22:58:21 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1838d5d0a05c23e9a823d4624b4b8f9bf68594819e3c09178b5c7319a47922e6`  
		Last Modified: Fri, 09 Jan 2026 22:58:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf39573595d85cd25a776d142a44e8b5b7525df070de4a4f9479237478e4d1d`  
		Last Modified: Fri, 09 Jan 2026 22:58:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c58fae825ea6ef592a578b1fa197b6d648b55e0d8afced18d4370bae18b076`  
		Last Modified: Fri, 09 Jan 2026 22:58:22 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7144d3325b6386a594ee2afd95964e9e8e1920a59d7e2b821a731b42097bb086`  
		Last Modified: Fri, 09 Jan 2026 23:33:46 GMT  
		Size: 18.5 MB (18460356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6be3e9b918aac637735461636a80db8d3331280c8b844d43dd119cd68744c`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 1.1 MB (1127364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf950556bb551afa16655657967d3d29fa15e4ae93767499a273c07a2d05885`  
		Last Modified: Fri, 09 Jan 2026 23:33:44 GMT  
		Size: 35.5 MB (35523389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d24eda8427af09036d4e7f6e2603739c4fb898b1a1612ff15150975fb60fe`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11ee4ae1190315e72f1b0075b1fd11ad5f0f38123b1af0c3d1bb3e243825131`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38133b2c88f35e06049e0ef12a6e6bf31879896d48229a68e663a987bbedfa81`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011ccf11d974e2638b17f12ab62ce25314e0ecbff9afc86006abc7fab186bf56`  
		Last Modified: Fri, 09 Jan 2026 23:33:51 GMT  
		Size: 59.6 MB (59606384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353239775361c3d7839db15bb12d2cb36ac516575185dced5f91cfe3fac5af70`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c82ebdccb4dd639fdfbf48b7911659893cca049cf847e086553cae332d59209`  
		Last Modified: Fri, 09 Jan 2026 23:33:41 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:03205594bd907b6f3ab0eb73e555c7ea3d1e320b5e89d31ba6edaa127ef5f432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794123baadbd76508f7c7d7b7f9e41ee2c468f6717f84c07109e51004ec3faf1`

```dockerfile
```

-	Layers:
	-	`sha256:92144774d5dff7108a758d6401824454b2fcaf0d990827c9c1d6712ceb7310ed`  
		Last Modified: Sat, 10 Jan 2026 00:29:00 GMT  
		Size: 72.8 KB (72765 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:c9094228d0070aac6cc4e1a771b9302a776018f4cb55e8848048c5824c0e8b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261188975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcaef62101c3d89f425692192ea9b4c19d1de11f5bd02081e4b5d2356176954`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:47:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:47:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:47:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:47:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 23:03:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 23:03:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 23:03:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:13:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 23:13:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:16:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:16:11 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:16:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:16:11 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:16:11 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:16:11 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:23:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:23:20 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:23:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:26:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:26:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:26:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:26:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:26:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:26:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:26:27 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:26:27 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:26:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:26:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 00:26:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 00:26:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 00:26:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 00:26:48 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:26:48 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:26:48 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:26:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 00:26:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26aa0b573f142f9b0f172c963bb3cbd2fc47e006c7aba719760051d7862300c8`  
		Last Modified: Fri, 09 Jan 2026 22:50:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd55753e09c84743b992e07648ef45d19d821ef2443eb62a1518579258d07461`  
		Last Modified: Fri, 09 Jan 2026 22:50:54 GMT  
		Size: 82.0 MB (81981482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201b2deb0888c40ecce1a2d4f14cfa2b3b9ab027e9be6398bbb78832a1045d88`  
		Last Modified: Fri, 09 Jan 2026 22:50:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5b4e9f8abf6f58978bd390affe54a84725c4c948d49555ef731535c5fab7de`  
		Last Modified: Fri, 09 Jan 2026 23:08:17 GMT  
		Size: 19.4 MB (19422410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbb3831246ac801fd770c30e11dbd431601659326ba42866a7335be05e5be2b`  
		Last Modified: Fri, 09 Jan 2026 23:08:16 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f75ff59eec261bb69f1fcb8c405a51984640ac7f93a33f577816d878d1dc5`  
		Last Modified: Fri, 09 Jan 2026 23:08:16 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8c9aa150e82881d4a1a0fa55a091b0c6349c3578247da0c7f8277fb0e23895`  
		Last Modified: Fri, 09 Jan 2026 23:16:31 GMT  
		Size: 12.7 MB (12729301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80ffca7217a93e370b297e9b8e4547d6bb261b0b46c0721ef5a669a3742dc99`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0521963e3ebb6bc50e77d1168307215fa51dcd65db232e465ce21a6401f40a`  
		Last Modified: Fri, 09 Jan 2026 23:16:30 GMT  
		Size: 10.6 MB (10615630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c750ada00f77073fa28faeb927de92132185959efd681cf0b42cc3699a4e34c`  
		Last Modified: Fri, 09 Jan 2026 23:16:35 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3b1265c16694f6ccee473b28c6ece16a4f2464bbc7f2ca6974ccf4e3b06224`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b091b576569913305d71f05cf0bcca3476388dddfb028a265a41a019949e596e`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf54b90af778ec2d6492b02c8de85774d19c6109e22e51778db5863d9e28628`  
		Last Modified: Fri, 09 Jan 2026 23:16:29 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4da5031219b247f936cbb2538235acef5da48664133886047cc409cc593d92`  
		Last Modified: Sat, 10 Jan 2026 00:27:11 GMT  
		Size: 18.2 MB (18196426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6a0c742941c655a641f9f2cf9205a022cba329733d744e8a816fbe5c68654`  
		Last Modified: Sat, 10 Jan 2026 00:27:06 GMT  
		Size: 1.1 MB (1102750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3146ec89b31e17ce075cd9996b763608d4bf63554ceb6a9bbacdb59421f1c607`  
		Last Modified: Sat, 10 Jan 2026 00:27:09 GMT  
		Size: 31.8 MB (31769131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b660b4b7a26fc7735fad755522dd850c7a71f1448171a6d21bb63cdd2e6060fd`  
		Last Modified: Sat, 10 Jan 2026 00:27:06 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d74f4b4482b289b5127ee4aaf8137786babd90196dd281711d284bdbb635c7d`  
		Last Modified: Sat, 10 Jan 2026 00:27:06 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af4cd8f38a21b44021e3820e78c694ad034ffed1191a9f21971779ed10a1a75`  
		Last Modified: Sat, 10 Jan 2026 00:27:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71331ba72fb7beb8774424d18197788f46cb1659c97843c8c6962e39e130f8f`  
		Last Modified: Sat, 10 Jan 2026 00:27:14 GMT  
		Size: 59.6 MB (59603119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f813f10eed5d28745835ad7e2c9806923f79ae2702f248c6471dc08842899baa`  
		Last Modified: Sat, 10 Jan 2026 00:27:03 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7209c2201c3789d56aebb57d19b816f46a87d8c5d81e9085cb55e6ce2870e7`  
		Last Modified: Sat, 10 Jan 2026 00:27:06 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:55deb13ecabcbfd733c58ab3395032ef99aa6adb1bfd1d5ec2f0f7f4b10f4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a986e50cbf98853c1928a952c305befe94f7b0ce3ab5164295e1091e05a6897`

```dockerfile
```

-	Layers:
	-	`sha256:3fe4f081bf52df778ebee60755aa2bce3609cf646b93c04badf9b444c1ee1ffc`  
		Last Modified: Sat, 10 Jan 2026 03:27:43 GMT  
		Size: 72.9 KB (72929 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:0767c38d252998b0f83ec339f4b7af58df6550595b82571db1e764e512c5add6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250581972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23667a9d184ee8ad2436c6f07bc29eee4fa62293482cdebbdc0061d5b524c9d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:44:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:44:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 23:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 23:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:37:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:37:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:37:13 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:37:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:37:13 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:46:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:46:41 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:46:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:49:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:49:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:49:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:49:22 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:49:23 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:49:23 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:49:23 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:49:23 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:49:23 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:49:23 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 00:49:23 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 00:49:23 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 00:49:23 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 00:49:41 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:49:41 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:49:41 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:49:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 00:49:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb090f1d21d6c9cf3d4937306130af775c6b8f77b7015bbc3aeec7831e00cd`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6bcf417f4c97734fc37095a7f4c9b4cfa7d5b09bfe0c3da212d45e63079a7b`  
		Last Modified: Fri, 09 Jan 2026 22:47:58 GMT  
		Size: 76.1 MB (76148731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b714c6e3ee2e505ebbf8085d3c232291b10a74563d8e2886cc4677b5c8b7fe`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba97861883a05a5fe227b13559b8b9477552ccbce71a196429fdd7ba71d8c4bf`  
		Last Modified: Fri, 09 Jan 2026 22:47:53 GMT  
		Size: 18.9 MB (18860044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f877b2e5c7edf9f5fd98f943e52013a9ee513903917ac0e6697d9b819d07350`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cb1bd16c15ea76aea5f1cd5ec4c5f28d6739045d25f1fdb092673752891b9`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc8bbd8b22b2399367d574ae631ed3a6e044da705a84027e865f4b7ffee65da`  
		Last Modified: Fri, 09 Jan 2026 23:37:32 GMT  
		Size: 12.7 MB (12729266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa399bff53edbd66d0678ec48b2d99436e567f84059e4b96c88dd59b5fda5`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c3d8fdbcc4335f3898391a47378469d4e93d61f7303565425f5fa69091c822`  
		Last Modified: Fri, 09 Jan 2026 23:37:31 GMT  
		Size: 10.0 MB (10049759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577b47bc7ef386d5004a4df01a841f82fe6dcc2ca8d2412725d02b75203cd7b4`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be21a00827f7ca0124aeebbd2d30c8d3aa9aaea16cd45000ef758ae5e6e1622`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c20abdd97be432f13737033bbaa7badd860a10e81f73a74b45cc4c7a071d8`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa01db12881d90b659d89bda994b860374fffdc9488ebe6a51f311a74056b45`  
		Last Modified: Fri, 09 Jan 2026 23:37:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367fe6adcac4a6988d64ab933d4cda40d6cdad77f8bbcb66ea65ee64c5b7853b`  
		Last Modified: Sat, 10 Jan 2026 00:49:59 GMT  
		Size: 18.1 MB (18097733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc90c695e50edc6a99e887aa7d9be75a29887d85364b55c5956e7e2f122185`  
		Last Modified: Sat, 10 Jan 2026 00:49:58 GMT  
		Size: 1.1 MB (1093260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e4a13b5db4b87f3a58958bea330391acb4f2fa0160973e9db008ef07377a8`  
		Last Modified: Sat, 10 Jan 2026 00:50:01 GMT  
		Size: 30.1 MB (30054734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb6ab8ca134d9f62d985903435a485bd972ea41a9463c90bfb5564f05b8c19`  
		Last Modified: Sat, 10 Jan 2026 00:49:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cc49233d86c8bf7e2daae543597cfd0953ef932869e9eb1f211cf374f6082b`  
		Last Modified: Sat, 10 Jan 2026 00:49:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e9abbe2848cd6fcbf888d30d03549e990ca8cc693fa7e979cbe77b6815c84d`  
		Last Modified: Sat, 10 Jan 2026 00:49:58 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7129d12dd4f6820ad78c1a7ec9a4379aaebbbebe115c97099f1316a8aeaa87ce`  
		Last Modified: Sat, 10 Jan 2026 00:50:05 GMT  
		Size: 59.6 MB (59603234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75b0e308a81b5e4cc9bc70eda1539a167d7948046bdf7eae3c009a821c8ba37`  
		Last Modified: Sat, 10 Jan 2026 00:49:32 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ddc73c469b10a5e006aeda3437ad5ff4f8da4e48adce2e9a74f5f7076ff0c2`  
		Last Modified: Sat, 10 Jan 2026 00:49:58 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:e8a1e81c182e7ed30261e600722ef8b56965dc6671a0b0f32575765b75c1cba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc812e2566761d8609ea9012db9dd171de2cc995a46bfe68321311de5c01cb22`

```dockerfile
```

-	Layers:
	-	`sha256:f834b39c715a0c5ec4bf0a3b29654642378053a141426a64220d69f24ffb6ad4`  
		Last Modified: Sat, 10 Jan 2026 03:27:47 GMT  
		Size: 72.9 KB (72929 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:787d10f77274c3d0052435e3b281606fcf92df3914a864f7c220d4b571681c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283145750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a153a458d61abc96c068a1033450212c56405d383e2c519df0cee8f7d792e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:59:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:59:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:59:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:59:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:59:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:59:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:59:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:59:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:59:47 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:59:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:59:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:03:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:03:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:03:52 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:03:52 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:03:52 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jan 2026 23:33:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 09 Jan 2026 23:34:02 GMT
ENV GOSU_VERSION=1.17
# Fri, 09 Jan 2026 23:34:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 09 Jan 2026 23:37:43 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:37:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 09 Jan 2026 23:37:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 09 Jan 2026 23:37:43 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 09 Jan 2026 23:37:43 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Fri, 09 Jan 2026 23:37:43 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 09 Jan 2026 23:37:43 GMT
VOLUME [/var/www/html]
# Fri, 09 Jan 2026 23:37:43 GMT
VOLUME [/var/www/data]
# Fri, 09 Jan 2026 23:37:43 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 09 Jan 2026 23:37:43 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 09 Jan 2026 23:37:43 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 09 Jan 2026 23:37:43 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 09 Jan 2026 23:37:43 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 09 Jan 2026 23:38:01 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 23:38:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 09 Jan 2026 23:38:01 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 09 Jan 2026 23:38:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jan 2026 23:38:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5450c35b859fdaf015417139d60e46d501038ffc84cc8cfc56dd2d5355c291e7`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5137a3b0176cac5ea342caad3a5fed814bacae3fabb829ace4fff233766508`  
		Last Modified: Fri, 09 Jan 2026 23:04:33 GMT  
		Size: 98.2 MB (98165645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050f54b346ff672578f78bee0b344b2ddd3dd2d8587f73dad29a1d10b3eaa565`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a98881c16a3d3c86e2e550c716fdbbfc9d7f85edbb1bd13d1c2463ce7e47fe`  
		Last Modified: Fri, 09 Jan 2026 23:04:24 GMT  
		Size: 20.2 MB (20159105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4faff44f0315a732368c751c54fb9ece3b2d84d49f1948b8fea6edeb68e71`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc6e69cb81880398e08379512ccf7a063f25f76ea74757ade4529ccbc5d213c`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693adf2964126a60ec236e69934b608eb6fd2225204b7df56c27c44f91fc9aa`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 12.7 MB (12730675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41aad276a4320c26af9db8dfeac2bb3f08c947baf9f4e86bccb8fd602bfa9b6`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af918158cf3fbc2cda0b5b2577db9714e178361af9c7b03acb51165d283466`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 11.7 MB (11691135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cadf7ca47ca804b8f79ddcfce6796d0126fb1aa1e8ce3ab061561ae510efc05`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f24cb8f109e2c487763d16c0400296952446291689f7649de663998a92f3294`  
		Last Modified: Fri, 09 Jan 2026 23:04:22 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7951756ef41df75cb2b46cf57c2538cf7e574060c53561cf399b5e27f8f4e039`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d812e03e543d6608fe721dfbf2ae7d05087978b232bd6957aca0ce66dc999f04`  
		Last Modified: Fri, 09 Jan 2026 23:04:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb47bab4558e45ae44129f67eff536375bfc5f6623299c9765bdb5890b112f2`  
		Last Modified: Fri, 09 Jan 2026 23:38:22 GMT  
		Size: 18.3 MB (18251794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a06fc97de655cec06218209a291956896101e18befac435e60c87e83b8ec986`  
		Last Modified: Fri, 09 Jan 2026 23:38:21 GMT  
		Size: 1.1 MB (1059350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce1015b551f64d4e85744b446ad9fd5b6ff249329a5b029387f6929026edaa`  
		Last Modified: Fri, 09 Jan 2026 23:38:23 GMT  
		Size: 33.4 MB (33368826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946540ee1923a6b416a69cf5c1fe9d058ace9091f4c32c1e874d058e2868ba3`  
		Last Modified: Fri, 09 Jan 2026 23:38:20 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4984773d1dea92c5a591d18b5f46c7e7256e6e8b6da8ff3f6f3670ccbe9736`  
		Last Modified: Fri, 09 Jan 2026 23:38:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84004353a66c6dfdffafd2b0c00abb8617eb017edec7013e685cdf2ab358fa14`  
		Last Modified: Fri, 09 Jan 2026 23:38:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8932fdcb40e84d7620dfc9dd01737fbe8d9f00daa6b1c1c4f9b19cd29e1c607`  
		Last Modified: Fri, 09 Jan 2026 23:38:26 GMT  
		Size: 59.6 MB (59605868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458543219f4268d217290d15c4a54ff48e6c26e2dab1724c6425c5ff4c116360`  
		Last Modified: Fri, 09 Jan 2026 23:38:20 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aededc09783eb2684a80d4d78dd24fabd812a2ddc13a9fb76f389f71e08d55e`  
		Last Modified: Fri, 09 Jan 2026 23:38:21 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:d26c273b75a5ee1c0f6aafd63bed67580246e40d88459372ff287037dadddb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 KB (72973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6ea8aae33753c08b83afea522e1c42e95a4e8a6dc974c7c394527c7b015d73`

```dockerfile
```

-	Layers:
	-	`sha256:88871cfcf549be21732547aa5c1538e96157b67b8c344885fdf800bd38ce7e56`  
		Last Modified: Sat, 10 Jan 2026 00:29:08 GMT  
		Size: 73.0 KB (72973 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; 386

```console
$ docker pull friendica@sha256:6bb970f79d19b28ea7d1b348fcc577579e760e1195c2820084d119983ea8df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290525032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa83344ddeff2ab201ce8b440be5c100440ea41b61d35cf9a97c432d364aee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:29:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:29:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:29:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:29:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:29:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_VERSION=8.3.29
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Fri, 09 Jan 2026 22:30:04 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Fri, 09 Jan 2026 22:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:56:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:59:35 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:59:35 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:59:35 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:59:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:59:35 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:04:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:04:25 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:07:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:07:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:07:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:07:08 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:07:08 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:07:08 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:07:08 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:07:08 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:07:08 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:07:08 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 00:07:08 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 00:07:08 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 00:07:08 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 00:07:26 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:07:26 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:07:26 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:07:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 00:07:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457d1ccad785195cd8bd82a3434569a2b2e357a1e61f19131ca5652d6ce1ac53`  
		Last Modified: Fri, 09 Jan 2026 22:33:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364dc2436467be37a657a53e4ecffa17670f77073ee1599544d346c68ed4637b`  
		Last Modified: Fri, 09 Jan 2026 22:34:06 GMT  
		Size: 101.5 MB (101518476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e91d2d69f9a2a540f430078be65bc6735b8b4cec70665b84ee7624f3fee76b`  
		Last Modified: Fri, 09 Jan 2026 22:33:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdbe4f2d1a8e1de791bf090afe58aaae18fca4fc5bf2ede2aab1b92053453ec`  
		Last Modified: Fri, 09 Jan 2026 22:34:01 GMT  
		Size: 20.7 MB (20658421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2afbd5f39f8a477d14e01d1cbd145a2ce6f152b25941e7afa835d339487525d`  
		Last Modified: Fri, 09 Jan 2026 22:33:58 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5da1d953a49f3c537d3ad2ffcf63ba53f03caea7ab18eac3348b3760ac7dfbd`  
		Last Modified: Fri, 09 Jan 2026 22:33:59 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95582bd179bf4d6d9a93de4217e75c295ffbda76e39c03736d42038bde95a8a3`  
		Last Modified: Fri, 09 Jan 2026 22:59:55 GMT  
		Size: 12.7 MB (12730169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b40d3dd2a8a54d18b6eb2d7c702aa87861b10ca2b307509f0cc15aaeaa318a`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995aedc2bbb69bf77467aaaa0346621c1abb1537801ac984f57a32b6797c6ea4`  
		Last Modified: Fri, 09 Jan 2026 22:59:54 GMT  
		Size: 11.9 MB (11884978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded6c2130cabf4d29ca0e90d8573dd5f361b951da4cb960059ceea48810a587`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312200252f68fd97203e4e64c48a3fd2a78c33442213e283e099c59501274f60`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59300bc514fc6ffea72ffa786c8d6f21289144365ea91c411f98e175fe5243b2`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d992366c38238f28845e95d60c74b0d97fe2596c6ad85ff3337515a598bc0a92`  
		Last Modified: Fri, 09 Jan 2026 22:59:53 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aced69f9600ab8637c30d2ad87a9f402c092817fe4452e305ff49ef8fd5d5b1`  
		Last Modified: Sat, 10 Jan 2026 00:07:45 GMT  
		Size: 19.0 MB (18983024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f11b6de3503a23b728c92b99cf56a9a21e535b80c20544a386c2cba2aa4de4f`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 1.1 MB (1102061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b17c5457449c563af1d5edb44d2501f49bcc741f3f9f1bc577c2243d7d6d898`  
		Last Modified: Sat, 10 Jan 2026 00:07:48 GMT  
		Size: 34.8 MB (34822260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5125836b8de6c167f1329d62474a062a487a33cc492ecd3eb74363675419026d`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4397b1dd536c87ccef441979c8ad30e6dfcf78f149aa32a1f73a79bbe29d73da`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e12f577966b2802544f255708ad8aeee7ad281c4d3ada4535923b88f3ed919`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbde05a07b33075f2190ab96e9dc13c28aff866a02d78f96b486a49aed93e8`  
		Last Modified: Sat, 10 Jan 2026 00:07:53 GMT  
		Size: 59.6 MB (59604723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca27b53f755bf9ce5fca9b98015325dc1debb2cc1e5c24c04f8218fb41f532fc`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ba3f6e9adba2e894df8c7e0e25a403e2ceddbe8096c92f1d0a2e61c959073c`  
		Last Modified: Sat, 10 Jan 2026 00:07:44 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:4819f437cdb7a6b1333425bf05ebcace39843cab00cc4766b04e46ca31a4f66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 KB (72710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a16eb9e195314bfa5a43a2106496c29c314e3ae02a6ccb5df03d0096883699`

```dockerfile
```

-	Layers:
	-	`sha256:3ada89197c088915ad88ccc216e2022830df5b12e6984a6b003dd29f393d2744`  
		Last Modified: Sat, 10 Jan 2026 00:29:11 GMT  
		Size: 72.7 KB (72710 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; mips64le

```console
$ docker pull friendica@sha256:9d5819473bcf6c736be887a80f40e89239b45673be19bfbc159b1855dc27cc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263692094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a50a256d61cfefc3855bfbd625d3d323dc3260f8aa098c1c52e4a430edce95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:18:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:39:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:39:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 02:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:10:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 04:53:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 04:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 04:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 04:53:24 GMT
STOPSIGNAL SIGWINCH
# Sat, 10 Jan 2026 04:53:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:53:27 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 04:53:27 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 04:53:27 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 06:35:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 06:36:35 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 06:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 06:48:43 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 06:48:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 06:48:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 06:48:45 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 06:48:46 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 06:48:48 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 06:48:48 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 06:48:48 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 06:48:48 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 06:49:46 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 06:49:48 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 06:49:50 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 06:49:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 06:49:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d9cabd4aab99e194d4a41705774411b061e905a5607b5d68428e6c0fdfc3f`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa90b950d6df8880366223e469aa2861d9bff3782a34bbbbd8c49d4d03a522`  
		Last Modified: Mon, 29 Dec 2025 23:38:16 GMT  
		Size: 80.7 MB (80670513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39959c61c1a601c13b85fe9f2c5c8646ffe26d790e73c6bfb044a1a8b6891d0e`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd3e0ce24ae30c711e9419a264d4d93fce74a5c8942103ed45335be3ce91d5f`  
		Last Modified: Mon, 29 Dec 2025 23:59:39 GMT  
		Size: 20.1 MB (20077244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66299e8474ac8c18bf4447b629ee9d516ca68ec5591d0b782108643a83b38af`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252fef5e44ae8f0167582befd01c30b3a3ff36ecb05a852ed19c145bc6d5c389`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2517ba538e65aac91e90741b78ea33277b591c2cf858ceca9083f796a89ce1a`  
		Last Modified: Tue, 30 Dec 2025 02:26:53 GMT  
		Size: 12.7 MB (12729094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8a6ab7831cf57fff1c762f8cae82a8944e319d01d7bd4f9e5200e298f241cd`  
		Last Modified: Tue, 30 Dec 2025 02:26:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f356c557382aec51a68da371ff5cbc3f40bafb97153d29d0ec558a25b6dc30`  
		Last Modified: Sat, 10 Jan 2026 04:54:14 GMT  
		Size: 10.7 MB (10746335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99427c011b9792d01eaecb5fd36a0fb30b485bb02b0287b7f162bc029346d02`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97513cc46e69ba1aac8556be8e556893a0a2c62a71b7db73b366face2e18313`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39330457423a74d9f33660e574a782d05fdbeeea9413aa5fdbc40c2fcb55abfe`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbcf6a4738869ac3ebb85bca1b3c2b41afe41e213e62e2d66f7e92507462a67`  
		Last Modified: Sat, 10 Jan 2026 04:54:13 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac180bad3076c672da6dc391e6c5c520927a6b2e95ba7c797148e18514a9cc3`  
		Last Modified: Sat, 10 Jan 2026 06:51:24 GMT  
		Size: 17.7 MB (17738946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f223f05cbb9ef4ea15e4ff331aacddec48bb669f00037975647a4e2affbf8`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 1.0 MB (1012565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528ea40e15d8d35afe62586282038b0c02e9ee1eb18423a53db3ce8f89b8a59`  
		Last Modified: Sat, 10 Jan 2026 06:51:25 GMT  
		Size: 32.6 MB (32587060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8762306849c53c0ce36d156352d1f793497cb3b2094f578734722e98840bf5`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1a6f587b2eb7fd6ab1f5427fa6e01939a012d03e23bccbf9d3818c15b272e`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75516c7b06069dc6e3cf84a510f0d322ed14eb07b05ef3869ef0b55542bf5c7b`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480f6c72f279271140cb0ae4dd20248237a1101fadfbea48ed379c9d44102373`  
		Last Modified: Sat, 10 Jan 2026 06:51:32 GMT  
		Size: 59.6 MB (59605350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79ba5aa723fb8405cf94055ac65a52840dd6107d821239bf728d94d969a657`  
		Last Modified: Sun, 14 Dec 2025 07:12:01 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7804a0220c29b04d49bfe41c38b005c06a010013e49f9eb989184fa603b453d`  
		Last Modified: Sat, 10 Jan 2026 06:51:23 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:3c705144c14c3ec392b545db5d5ef9fc9c0960f89f5bfed9bd13cf4aa9938581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 KB (72857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae73daa573b350d63bfdcd01aa3ee89ad430ec3337bb5f5eb49d5c22bfa545f`

```dockerfile
```

-	Layers:
	-	`sha256:86c5e52b96f2677905c689e4ac132d0e57bff8f74bb2152334992e13e75786c1`  
		Last Modified: Sat, 10 Jan 2026 09:27:32 GMT  
		Size: 72.9 KB (72857 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:d77e2a0e523d2fee27f24f3e575f0dc14b8f7b753408cfbfd5587ca82261f1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296231008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f7c84cb4214cb80734c6aef856370ac8e15a13d83369164d81c981f53bc27c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:15:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 30 Dec 2025 02:38:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 30 Dec 2025 02:38:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 30 Dec 2025 02:38:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 02:38:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_VERSION=8.3.29
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 30 Dec 2025 02:38:26 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 02:38:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:38:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 01:38:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 01:38:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 01:38:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 10 Jan 2026 01:38:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:38:44 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 01:38:44 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 01:38:44 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 03:04:51 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 03:05:17 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 03:05:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 03:11:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 03:11:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 03:11:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 03:11:52 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 03:11:53 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 03:11:53 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 03:11:53 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 03:12:29 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 03:12:31 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 03:12:35 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 03:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 03:12:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93a9966845dddb639588fdcde0ed0ecf405e81db5bf3e7b306c9cbebf976cb`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226cbc8a9cbea94e5a9e2e037754124cee088acdf931d11622ed35b2aabbfeb`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 103.3 MB (103328995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20082871cd07652f43cb1378561dfdd8cfbf23782814ff423bbb205eeab4afae`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb4530d72cd41f205428c35fbed64b09ccf2f3f4fbbaf043562a88e6007268e`  
		Last Modified: Tue, 30 Dec 2025 02:42:48 GMT  
		Size: 21.3 MB (21317921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5b57248912e84cfa43adc472de2f9fc3b5b62aa101d4e8fc58896028d1d26`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7e387f48c69b88a5fe2813456ea23e7fd37b459cb903368e549b64633df976`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1e80a0bf2e049c7b710907e4fa7f6968bbacfd160cfeae222ce034a496ff26`  
		Last Modified: Tue, 30 Dec 2025 02:42:46 GMT  
		Size: 12.7 MB (12730458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fe507b26bad848467f50075fcd792df27ab6248bcc0ea98acfee5d22e8f27`  
		Last Modified: Tue, 30 Dec 2025 02:42:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4538a08e0234705391bfd4536f2024b4fb20328d5d1515d0301f81a3d58bf4a6`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 12.1 MB (12089620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de96dd923991ddd635c95d691de552987785a7ef4ac75dc92976abbea456d3`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ad80e117b0884e07cad3cefd604ec298f87f1df0a1b929ea97a3b5af8360f`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9226b77cbb106247e184770ec3c644b5f6077c34d3f869dfd109e5db682e254a`  
		Last Modified: Sat, 10 Jan 2026 01:39:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6375ee876d68a7f278b10602fc2f2d53c67faaa05969d12b9716bdb8f25f`  
		Last Modified: Sat, 10 Jan 2026 01:39:18 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172f526ca4e86534b3297a5eac35be3c066b7fc6a8d4651db6b93c44db6100d`  
		Last Modified: Sat, 10 Jan 2026 03:13:14 GMT  
		Size: 18.6 MB (18578952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd16674efd4f38c34169c6d3314bc38dbb08e5179bb2ec93676bce4569061a8`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 1.1 MB (1050397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fcd39f83fa98a7e9f6bb59acab3eab3306f0b52be03b733c532eccd25988a4`  
		Last Modified: Sat, 10 Jan 2026 03:13:17 GMT  
		Size: 35.4 MB (35447767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3cfab89a7322006fd057d1fc49a0d0665bfd9254d826622294d8746c07b11`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6db5b19509f41c4c5c3096e908353e50ad2059fd602087f9cb3161c49c365`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eaeb7babcb84f639b6947d0a04b75d87803203018cd93b06ca07f2558f70ad`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c21e16929ca9f84a8f5c3fa9abbb859b5868d358d861522feb5a912c230b6d8`  
		Last Modified: Sat, 10 Jan 2026 03:13:19 GMT  
		Size: 59.6 MB (59606900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a3b9b146feb6a00485769f8020d1f72be8c6c0a8dcfb5d1aed8d10cdc94da3`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae556488fee496e380759d1cb6454c84c1680988813916241129cccc85743d`  
		Last Modified: Sat, 10 Jan 2026 03:13:13 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:860e998069ee10f09b5615d2c424b4faf322a50a24cebfe7beaf7a759defa7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7bce513353bf146d9c9cc8f5ab37bfc31a30cc0b904f1caf425871a428838c`

```dockerfile
```

-	Layers:
	-	`sha256:08dd4e926cdb1907203efc774a554c76cb9da9dca21617df5c472ac0e499a6e8`  
		Last Modified: Sat, 10 Jan 2026 06:27:32 GMT  
		Size: 72.8 KB (72833 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; s390x

```console
$ docker pull friendica@sha256:a0b562db0bfe0951082f59e074123164896e063224cffda3994b2de363124636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261265182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dbde286595432df41983be3110bfbf900e49bac141afaa50c3484bfbd065d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:24:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:24:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:36:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:45:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:45:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:59:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:59:19 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:59:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:59:20 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:59:20 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:59:20 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 00:38:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 10 Jan 2026 00:38:50 GMT
ENV GOSU_VERSION=1.17
# Sat, 10 Jan 2026 00:38:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 10 Jan 2026 00:41:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:41:19 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 10 Jan 2026 00:41:19 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 10 Jan 2026 00:41:19 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 10 Jan 2026 00:41:19 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 10 Jan 2026 00:41:19 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 10 Jan 2026 00:41:19 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 00:41:19 GMT
VOLUME [/var/www/data]
# Sat, 10 Jan 2026 00:41:19 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 10 Jan 2026 00:41:19 GMT
ENV FRIENDICA_VERSION=2024.12
# Sat, 10 Jan 2026 00:41:19 GMT
ENV FRIENDICA_ADDONS=2024.12
# Sat, 10 Jan 2026 00:41:19 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Sat, 10 Jan 2026 00:41:19 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Sat, 10 Jan 2026 00:41:34 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 00:41:34 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 10 Jan 2026 00:41:34 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 10 Jan 2026 00:41:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Jan 2026 00:41:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb418c0e5abcefe16acbc6e83182df41a4844e89a661b7628f7b0852127c87`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbed6618c1961e2a7b7cf2c87e46f37dd87a16548388c42e37807bf2ce70d12`  
		Last Modified: Mon, 29 Dec 2025 23:28:46 GMT  
		Size: 80.8 MB (80826406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdd0c0b33812eb4b7f25ae54473174aebd54cf322e1c27b866650bf4f1c6dc`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222bc849e1b19371c05dc68d739ed0f184d73bbb8532c19f810ba988bef7b2ab`  
		Last Modified: Mon, 29 Dec 2025 23:40:12 GMT  
		Size: 19.9 MB (19909960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89757ebcdcc864a57a0e2a372eb3540fbd9b10f5a4de7457f350eaeae6a38b35`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd1a00aff1b003f8f4201db4bbce376688e04da2e77809b06123ea3d73eaf17`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd44b0edc854d4c70a677e49226387ab8ab9acbded814f93b65cfa17e7e4afb`  
		Last Modified: Mon, 29 Dec 2025 23:48:00 GMT  
		Size: 12.7 MB (12729674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85bd2fb9f05a92d50a1166ca11246d04f8b63c3a052843ed21a62f5a938e3e7`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee1e7d723d1529427633d1266f3440b5268bbbee89860b5f860e3618579a754`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 10.9 MB (10895817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fd70d8f604ec41e1920fefae4804ffcd9b7976db49138e1ab133c72af7a26e`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2302490d3ad41ec798c7e9599cd079a85af736b2333b12b27c7569aa3d0b4692`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cad21b4a4cce962d44a7d2f3a9ff183cfcda1e0ab6e18d2c06186934b0f104b`  
		Last Modified: Fri, 09 Jan 2026 23:59:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d209b72318af561448271e5264639c438520ca684e8297cbdc412cf6a92bc0`  
		Last Modified: Fri, 09 Jan 2026 23:59:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb4a67296ea2863e186c1a231a7b6301e717215854d72ab5539dc6f2cb367c`  
		Last Modified: Sat, 10 Jan 2026 00:41:59 GMT  
		Size: 17.7 MB (17736880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d4a832437e80a6bfcf982c698719c895225ad3474901cceadb2062c04494ff`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 1.1 MB (1091963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68fcbd20bf36eeb54f9cc1140567516f2e171fcd0826a925b1e5e5fb01339b1`  
		Last Modified: Sat, 10 Jan 2026 00:41:59 GMT  
		Size: 31.6 MB (31576068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cf62315b485df0ca99daaa5b918a7cb817d71946d3a261b3d196d539e1cd8f`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e67c4317eab5f9b7517470edfef9f81d18e0941de9c5acded03e1581e7fec5d`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2a3ad0e828d7a5468c098379203aa22d4918fdd5ff7e4ce2933e978da55e6b`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc2dad349a5919706f332bed26ed1ad4313c1fa4f2202015a53d0107bdec3f`  
		Last Modified: Sat, 10 Jan 2026 00:42:05 GMT  
		Size: 59.6 MB (59602863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a460da22bd774059938133ea77f4a6f7141675e1b4183cdfb05553771d081a2`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c083c722630ec0d64a32ebfc799104e31bfe726cb2339a8fe008ddb6dd23acfc`  
		Last Modified: Sat, 10 Jan 2026 00:41:57 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:ff0d2d398ec28aca23479e27fb5afc72be0700591c7293af7d7115e6aa64db77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 KB (72755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbea052ee919bba17832d8029f0c37862ef7af9b770dc891ed80543e715f8ac`

```dockerfile
```

-	Layers:
	-	`sha256:320a3ad210c47a55c12898948edb90af8f240e15bd91674906ef8708c4ea6b08`  
		Last Modified: Sat, 10 Jan 2026 03:27:56 GMT  
		Size: 72.8 KB (72755 bytes)  
		MIME: application/vnd.in-toto+json
