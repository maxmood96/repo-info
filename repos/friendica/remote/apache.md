## `friendica:apache`

```console
$ docker pull friendica@sha256:2971ed9b41f7c9d40c0de505dfe3906a079dd32a1fcaa3a28e08df18d880f3b7
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

### `friendica:apache` - linux; amd64

```console
$ docker pull friendica@sha256:692934a877c910723f47f7f4c73e2b4c8ee3968822e3b023132837987c58e7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291678410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eb37bd7f66026de3bb81c01522e411c2fc0b8d83c20c9be37bf9bf41cb482c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff4e528452292981a2ac93047f835ba9d486640caf7845a91952e60263df9d`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede17ea19b1ab4f341ba469f678704a18b6c77fef12b1a304c4b938784dfbcd1`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 104.3 MB (104326256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe273df9238b3085e53711d838ea656926836c275d4db249792a8c37d95a6f`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d14161c76a807519d8ff6f7b24d84c607780295847efb8696de2d686181ff`  
		Last Modified: Wed, 21 May 2025 23:18:50 GMT  
		Size: 20.1 MB (20124180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f091f3dbb2f1fbb15d87a4cb5e7c7a5cbb63b65f53ed3495b52b19357fb35`  
		Last Modified: Wed, 21 May 2025 23:18:51 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ad1b79a553bb2180c567693bbe8f9196d637059f644585439027a4dcd37f8c`  
		Last Modified: Wed, 21 May 2025 23:18:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a05f9f2c31f13b756b5c4961f0cc54e6c5c11a0b359451bf3964b2ef77e4d6`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 12.7 MB (12694937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7385e8172628456b50ad41a74dc5bb181a3a701edd8ddcde52d2b305bb0a09b`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0db1ed3ca8711c9d13321aceff6e9b84b1beab2a974aef32d542263f0fbb0`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 11.7 MB (11657661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b5d65604733e42071ed5c3261ca88c0c62bbfce0cc15ab3473aaa6463b2d6`  
		Last Modified: Wed, 21 May 2025 23:18:52 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f1574d2c458aff78243b3bef4f1f6b79d08495928d0c432430239bad297a5`  
		Last Modified: Wed, 21 May 2025 23:18:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9242b0c7ae99e2b08c75b6b020e18f470fd40c5ed5e3872147af8902b346735d`  
		Last Modified: Wed, 21 May 2025 23:18:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bf759c7236240f872f6e6fd1529b3eb0d2a5e6c86eb0ca84f68002af1b1314`  
		Last Modified: Wed, 21 May 2025 23:42:57 GMT  
		Size: 18.4 MB (18388751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6027254df69900fa26d5051504e82656a8551a0d90c8ab3659ad704e6855ad56`  
		Last Modified: Wed, 21 May 2025 23:42:56 GMT  
		Size: 1.1 MB (1126946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd747568b36ef17965e3f1905f061b07d480f39a11882431ffa83b07dae0f9fc`  
		Last Modified: Wed, 21 May 2025 23:42:57 GMT  
		Size: 35.5 MB (35518326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f6e56510708873066886f85b6e97e4345fe2c9003efa959b7fa038a878693`  
		Last Modified: Wed, 21 May 2025 23:42:56 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fc55769d6bc65133d0dc2818c1ca1ae483bbbd945cad2b90cc10ea1e5635c8`  
		Last Modified: Wed, 21 May 2025 23:42:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910ceea9631101438a24e68f315815d2f668815255c79cbe770665b3fa90fad`  
		Last Modified: Wed, 21 May 2025 23:42:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed474d0235d7b2fb8c97042b1a20d5b0c718b6af5ff84c9c25062c1607b5b82`  
		Last Modified: Wed, 21 May 2025 23:42:59 GMT  
		Size: 59.6 MB (59605151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f8d670f6ea0d6cc6782665dc07899a58b8edbb96ecbde5026c9e44321cdf3`  
		Last Modified: Wed, 21 May 2025 23:42:58 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0732b6b678697f4636c105b2f4e8265fae311bd6f23a765d088ce85df7827d`  
		Last Modified: Wed, 21 May 2025 23:42:58 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:5e729bd466492d137ddf19702df40816f5e9412ac61f7df57a4fcd71ee8447ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 KB (71268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7c5f27f0961312e82c51279a4c0e39e0b0bc28e49eed4c3239b20cf459d75d`

```dockerfile
```

-	Layers:
	-	`sha256:d56aef1f6678198beee9d08a4d4a8c65600283e2d777dc3f4a31957abebd0b9e`  
		Last Modified: Wed, 21 May 2025 23:42:56 GMT  
		Size: 71.3 KB (71268 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:d3c9f35c509769d40cbdb6932151fc1c3324a0ea11cf7cc941208c36dc0b3efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261057984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a53cd0443e97fb2f621e6e0ead18a466b6556b92902740f7be301d9eac2bcec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630a0ae6a7caa13c26c641757aedb6f2a685e945563086d454f01db874d5a4e`  
		Last Modified: Thu, 22 May 2025 00:01:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1543f1d03f96cc1c05ba7756b5950bbb8edfd3038bc0902f7bd06c8b3a5a6`  
		Last Modified: Thu, 22 May 2025 00:01:50 GMT  
		Size: 82.0 MB (81970289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1f2e7aca197ce584722af1cb59310256391ea143b4eee91fe64249d0f64ac8`  
		Last Modified: Thu, 22 May 2025 00:01:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58b58ecad378e2c244a47b087001bd8dd7a6bb20346f6a44056db42ab3a5ce`  
		Last Modified: Thu, 22 May 2025 00:06:36 GMT  
		Size: 19.4 MB (19419290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689f2b7224a1481ccb5f31a4a4189cf4eba4409cd5baaf7402ee9bf4a6ba1d7c`  
		Last Modified: Thu, 22 May 2025 00:06:35 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e190f82563d835d64144f74a1701508a80fd49ac413b53cda42a431d89cf4b`  
		Last Modified: Thu, 22 May 2025 00:06:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e3505ef52c3447c23905ef5720ea48318bba8d2d9c1afe16b2847c7ea108c9`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 12.7 MB (12692927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c83a05b7dc7e95053753fb0afb429a5b95164d0e1b4c2023b4b2c66f119484b`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cf948e234dd0fb5fdfe8c8467eab33fd34c277e0dc67a805bcb0a2a1ee0e1`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 10.6 MB (10628699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97453db94cc98168d4e7824a7a734d55ccb22b0255494f3fa0060db19b09d4`  
		Last Modified: Thu, 22 May 2025 00:24:18 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b5e7eabd43b67e84656682d9bdc1a51256528424a71c9ad78c6b1d3bc1698a`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927c40e88e5cb098b9ee425dca1ec33cd8fb2bf5fa57e85668512f9e2e410a60`  
		Last Modified: Thu, 22 May 2025 00:24:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a81ef020c58d4f5aeda29bdd2640aaab3c754476c3d889a0b86e850cec6465c`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 18.1 MB (18109841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcdadc8ddf7e888d5c26becd7eb0822977e4494264248cccfb06efd05e45d5`  
		Last Modified: Thu, 22 May 2025 04:50:27 GMT  
		Size: 1.1 MB (1102626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e235a124f0df46904bc480f4b2a226c3afdce309d9f153867a60d473ba5e28`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 31.8 MB (31763758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d722f27f8c45b0c7e58d01827f36df5b9efb0484516b062e9136690487de7a`  
		Last Modified: Thu, 22 May 2025 04:50:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f6401cadbf4cb7a614f6cd5612895d0de92cc2d04f281836bece42e46a56a`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ffb8e3be806dd39579f249b47c2eafa06be5bfc9185cec7c17fc61b70c6cf9`  
		Last Modified: Thu, 22 May 2025 04:50:28 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909b458eb16943a93a1a6ca3ba7d5b27f3ef43cce39d85c4109826ebf9ca7304`  
		Last Modified: Thu, 22 May 2025 04:50:31 GMT  
		Size: 59.6 MB (59602770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23ddf3458cd5453f6de3b0c3b616c9ac3733f7bbf41cddf18702af7d4f6dbb2`  
		Last Modified: Thu, 22 May 2025 04:50:29 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540e2072f4e3ddbe838d85593950995203902209cd3a3494633f6d763095c01d`  
		Last Modified: Thu, 22 May 2025 04:50:29 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:3e045126b60217bb8d89c6a29c3005d91e99391721da74b6881b7803ec110615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 KB (71427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6432f00f1a22bd69ae74bd105ca28db4caa49f93bd7568f5e38a8514fe3784`

```dockerfile
```

-	Layers:
	-	`sha256:adf12ed60ef0e14680166683e29b199208e3fea7b37cc3c69664577a7f175cec`  
		Last Modified: Thu, 22 May 2025 04:50:26 GMT  
		Size: 71.4 KB (71427 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:df3826ac88145356d15c868ffe6bc53fe6c53bf375f7392d954daed188b21b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250464607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb36e273d4f3aeac28e395e980e30acc2d06288aaa42ab363a824cc892afe93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb081af16798c509df91bb641dcb17bd3d33d61f0cf2bac99faf83bffbd9b7da`  
		Last Modified: Mon, 28 Apr 2025 22:37:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf0e8dc8cea29863841153fe9f3a8f89bbb039cb649bf7121f6bd16afce897`  
		Last Modified: Mon, 28 Apr 2025 22:37:33 GMT  
		Size: 76.2 MB (76161444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0d9733969300ceb14706abdd215b86e83169f1554815cbb19abf8d4283b57`  
		Last Modified: Mon, 28 Apr 2025 22:37:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6f48e0c7265485795f32b113efa9b04a68faff23123e36dcc1c1409a0e2ebe`  
		Last Modified: Mon, 28 Apr 2025 22:41:55 GMT  
		Size: 18.9 MB (18857578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef6e5c0032a0aa361aa51604b1c53cc9877e3052605e5f873db12f418bfd7cd`  
		Last Modified: Mon, 28 Apr 2025 22:41:54 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d01a9a8ce471d95f06223a7d884bcf99a1eddbaa15f1e4a668e504b9bd3fbe`  
		Last Modified: Mon, 28 Apr 2025 22:41:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00061edfe4e406afa4aa8ec5e455cbfa02fb1e48bde365d770f7530f872d58a5`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 12.7 MB (12692880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f52e86bc33e41fda247977375499af31e3543860f6e0a825db503f7b3f94500`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ddc7d51077483608fe01a866cdd2de8cb567f5838f40bef17565435dab914f`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 10.1 MB (10052334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c49898d54bcbb53097b7f9341eba6689a3b4f9aaebe74ad22fcf060bb1f69`  
		Last Modified: Fri, 09 May 2025 17:57:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf783b7a7bb6ab4398b04011e22ceea4ed0fae19e1e310e2fd05252ec0d2a5`  
		Last Modified: Fri, 09 May 2025 17:57:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b56492d36e11dfd74e6455943015db808d78c91a92fe37dde3b407f475b25`  
		Last Modified: Fri, 09 May 2025 17:57:49 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247075413be4c95baf06067afcd2179bbd77e5782b931213a8c18a1292c03318`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 18.0 MB (18015704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9619e0fa15d445fedc4ae9c22a93222ae89292c347e95f7658083ed5f20d6014`  
		Last Modified: Fri, 09 May 2025 19:54:04 GMT  
		Size: 1.1 MB (1093105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4e38b1d96cf124c71ac7468995544d419975373eae00bebe03797e9cf0b7e`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 30.0 MB (30039696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a993a8f1fedd8903e6559e15b022a283b187b6528c5485d32da9f807e40e58`  
		Last Modified: Fri, 09 May 2025 19:54:04 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a089d13d798804230481987b59e765c257a1900c512e66b16e63a00c2b58b1`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41cca2d909bc570fb70b1c4abfc9e7632ec1cbed197ea9d754faab910e3af30`  
		Last Modified: Fri, 09 May 2025 19:54:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ab27d49a311e06560025d29c59c461e985b55b8858341e10b65a3185a1a1e`  
		Last Modified: Fri, 09 May 2025 19:54:08 GMT  
		Size: 59.6 MB (59602906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4cbaae528d12979de4394adef5bf09983f625b1d01e195997ba2a01b281d54`  
		Last Modified: Fri, 09 May 2025 19:54:06 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c32152adb6ae51d32569679630deb14450f866aa1b97f183c4e91f9749effe`  
		Last Modified: Fri, 09 May 2025 19:54:06 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:707f8b83eb43aa70f116b0ee87f5ffd16881d7104d7b1ed8b9f3879dd321c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 KB (71428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a68c74c3e45794f9731d17cb61e5f16039cb99898d6f5b0d1b5aad0b5cb6850`

```dockerfile
```

-	Layers:
	-	`sha256:cc6c9edeab477c4b76c6188a17c058865ed9ca867446d0bdd8bdaf106f547a1b`  
		Last Modified: Fri, 09 May 2025 19:54:04 GMT  
		Size: 71.4 KB (71428 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:6b93bc50254da55b7963db99f8692346e05df3563a988eebeba0c39ad3286a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282859632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcd99aeddbccaed1212d811c298a08a65ee67bcfcca2a828da3d9ce631442d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162264c942aa762db417d45ba0a061dc8a07fdceff32a29a2d59afdc5dce9f9`  
		Last Modified: Thu, 22 May 2025 00:16:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae464486e7a7b754207a11225be678aa24148395332f33c785867c1ee4adcd`  
		Last Modified: Thu, 22 May 2025 00:16:09 GMT  
		Size: 98.1 MB (98128413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa473689d317e799934b0b99abeaba5a91da4380c0b6148373000ed23bde9ba2`  
		Last Modified: Thu, 22 May 2025 00:16:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c2eb5e806f90915c98adca0127759107240352870bfe86a7178c29ff06f3b`  
		Last Modified: Thu, 22 May 2025 00:19:46 GMT  
		Size: 20.1 MB (20121045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0dcaea15d7a4ebb0f4028699191ca3aa2002cfeec7788806c673ebb001eade`  
		Last Modified: Thu, 22 May 2025 00:19:45 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e656b0988010277ad979af2247a277d3699b9eef4559bbf50725b446fb4510`  
		Last Modified: Thu, 22 May 2025 00:19:45 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348f8a5c7d38ff9d4a6ac85622b907b6638ea2fafb66f642f60a5aea9295c68d`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 12.7 MB (12694665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb922c0029f681cffc7285553daebf616bef66ed18a0231cc6e0290040db485`  
		Last Modified: Thu, 22 May 2025 00:47:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb25ea06c756635811426f88394a1c1cbaa648ba02ec7824b19d7253f685b0`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 11.7 MB (11680311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90280cee654716c2503e730efac74700ad9eefc7d8c4773d66c0d20cc6e08326`  
		Last Modified: Thu, 22 May 2025 00:47:14 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29fcacf279cb0fd4697d3a1e0220eaa4100a963bc43a5ea962ce9aa14e8075`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9af748e1436181f47bc7ea7cc9f6539654115603140e9a49de2bbe6235524cc`  
		Last Modified: Thu, 22 May 2025 00:47:15 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f17e7e04d3b38444cc650760af36589c1024a59a33eaf568a5aea87a822a5`  
		Last Modified: Thu, 22 May 2025 09:52:14 GMT  
		Size: 18.2 MB (18157968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579603592bfbb2f75cd7754f440265fea0e6965f442ef426edea3981395419a9`  
		Last Modified: Thu, 22 May 2025 09:52:14 GMT  
		Size: 1.1 MB (1059190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26237f4ef523d3c12d373cb6ae9e34c9506d95ecd58e3d5aa357102921ba19`  
		Last Modified: Thu, 22 May 2025 09:52:15 GMT  
		Size: 33.3 MB (33336240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef20d634a953ca1fe71d092b20e2d0d21f67d3c97ae44b66ec58a1b6133642`  
		Last Modified: Thu, 22 May 2025 09:52:14 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956979e70adec588eb276375d0e25399dd9201599e620f7fb0582dc1ca0b6192`  
		Last Modified: Thu, 22 May 2025 09:52:15 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc3a5a545066930cc8271ae2c7e074c2094cccdcf88fef22565a3cb53bba75c`  
		Last Modified: Thu, 22 May 2025 09:52:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b0aec4c806976bd227b680fc48e285abb0fe98bd488e10356b48caef1327e6`  
		Last Modified: Thu, 22 May 2025 09:52:17 GMT  
		Size: 59.6 MB (59605636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cefd5342344179a37d7a5342d3f85261ee6a4ba27f8dca11581b0a95329dea`  
		Last Modified: Thu, 22 May 2025 09:52:16 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e998a8b30b071f9b36718d6bf916a64eb0bce8b2ff5acc2833241a003a2f766`  
		Last Modified: Thu, 22 May 2025 09:52:16 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:29ff509ba37d325394d33abe1ece1cba0c326178aa54dfda3cb8688209281b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 KB (71476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa723b17681730bd1f352d8df0ec7f6857a0dd4a62c734a23841da94e423552`

```dockerfile
```

-	Layers:
	-	`sha256:c06e391df8ee7e3fc501fcb5bb5efee67017a12a6ef7d17fb7122e850ae11938`  
		Last Modified: Thu, 22 May 2025 09:52:13 GMT  
		Size: 71.5 KB (71476 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; 386

```console
$ docker pull friendica@sha256:58e10255ba278178f6556d8e86589f5c266909606e5905d6f4bbd347aa206102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290357663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d23569e090553eaad4c3b18f07794c8c43e3f28e058345805a6437801e05d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b3ae0a3cc1813c1af104d1cf7c4f2fb9834143d9a6f6542b18b9ac8a5011e`  
		Last Modified: Wed, 21 May 2025 23:18:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd423ffbb88db1940d66d06b0021abd7b5766e7188fb2156024e6509069352c`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 101.5 MB (101507449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711ec981d33e8b6d48b89fe12686a6b9d190c34f687d910e058ecce3225b34a`  
		Last Modified: Wed, 21 May 2025 23:18:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e078877c3eb19610f9232307a243240e94a8a7679f9e7c74f8ea3d7d015021c8`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 20.6 MB (20638515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7966f53e345e500f89d42fcdfb69088040771dd1788fea554be117e5258cd2c`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ecb17b503894af45c8bc7a0115aa16b3f9a5c8d615207905395af43786ab45`  
		Last Modified: Wed, 21 May 2025 23:18:20 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc368442cd4c98d41af593ce0da6968e85171c7d52ead09539f7f6e23244bb7`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 12.7 MB (12693889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1852c37f3556ec38ed1c1ebe24c27e384d2a8ba3b280601c53c9f75eb0adb6`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588806f719016cc417569c4caac2ff9ccdcb4b34f35df4e0657a1c01b037d19`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 11.9 MB (11884509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87e07ec6ac0571e93f9080d3bfa744e6b3f15dec788047d87a83bd7bd116e2a`  
		Last Modified: Wed, 21 May 2025 23:18:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6fc221041ccb0c7f1033ad6656bcabcb91c18e2b1a568d96497ffd8ad46c6f`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d7418adfdbef868f03aa9ba2b0d5c2e0dc5d0833a60ded5f483da4418c8759`  
		Last Modified: Wed, 21 May 2025 23:18:22 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c557896c110cb8acabee5713d853c2f5580fc1fea8e2959aecae2130b2b5830a`  
		Last Modified: Wed, 21 May 2025 23:42:55 GMT  
		Size: 18.9 MB (18893698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9b020248cc4cebf6a818ec82d14059bcc84668f0d18ef3ea5997a8ced42863`  
		Last Modified: Wed, 21 May 2025 23:42:54 GMT  
		Size: 1.1 MB (1101721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddafbe60572f0301837980fbc9e2970301961e8712dc21370438610f9f51692`  
		Last Modified: Wed, 21 May 2025 23:42:55 GMT  
		Size: 34.8 MB (34815470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177a6db81094b4144382d9f5952e4491e2a94ea7bede5e273afe91920003f442`  
		Last Modified: Wed, 21 May 2025 23:42:54 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d8739ba499f65b36e0bbe3b5212a9aa8ecd6a3ea8ec1cb87a3c38c4f0ee6ed`  
		Last Modified: Wed, 21 May 2025 23:42:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c93fb2885c590af88fd86ea45c52285864495438e6afff09f0f379787e3ed4`  
		Last Modified: Wed, 21 May 2025 23:42:55 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f823c2e66eb7973e7643b0369b16551182a0f109549565a2d0c7addcdace71`  
		Last Modified: Wed, 21 May 2025 23:42:57 GMT  
		Size: 59.6 MB (59604048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17facc9656fe5001e2ca8da0c2faec49c601c9777718fe99041054b14456a9e`  
		Last Modified: Wed, 21 May 2025 23:42:56 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696133d426b25e374cc2318f46b7e64c8e91f5db70051167b873f905b4d8058b`  
		Last Modified: Wed, 21 May 2025 23:42:56 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:62733567eafd1c492b41edb929d72f2f42e89283833c12e34dba245e7bcaea51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 KB (71214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d656fee88e6ce8871b3fe10bc985bcef1a8ab54db19cbc3e5698c3c256e7a34d`

```dockerfile
```

-	Layers:
	-	`sha256:ae020b595cb6c0259bcd508b441fbf4e9d3bf171849ca3499be08710be95e11c`  
		Last Modified: Wed, 21 May 2025 23:42:54 GMT  
		Size: 71.2 KB (71214 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; mips64le

```console
$ docker pull friendica@sha256:d76bed6f5ba016f8cf8a6261f90093cc684ac2d4e13feb35306c2eba78b34111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263528332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad65c3ce852557602187b65383928791ff4e8f401cf153cfb3f5987d6d9030e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e343296b3c4c73e7393ed7e975e096d3456974497f1542b5ded29fe811633bf0`  
		Last Modified: Mon, 28 Apr 2025 23:52:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b0bd4e1321051cfa09dfb6902859ff6e7b2447f11cced855ce09ed1bafd8d`  
		Last Modified: Mon, 28 Apr 2025 23:52:23 GMT  
		Size: 80.7 MB (80670410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4373130a8dbde2eecc875cae7f6cbf3eac8351ea553d2b6dd0b3cc0ae00fe67`  
		Last Modified: Mon, 28 Apr 2025 23:52:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56746e7214764a2245cd81e761a98bc9b2d38bb60993b2aee05668d56c16a8bd`  
		Last Modified: Tue, 29 Apr 2025 00:12:26 GMT  
		Size: 20.1 MB (20069252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1ae0bd7a891f0e4b151b24f787e34628dbc935f5716272c2c75ca07fdebb0b`  
		Last Modified: Tue, 29 Apr 2025 00:12:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bae42ff97aff3dbe0d62e06582e5344a420ce7bf0f97e842adae3bb17b01c`  
		Last Modified: Tue, 29 Apr 2025 00:12:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8a48666e99263ab500ca2a3162e408743d94da04fcbc48ab94d38ec619e626`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 12.7 MB (12692586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27aa2e6140cc3ea9686b1a2563c9de202cd78d97eb274ed418f60aa4b75e391`  
		Last Modified: Fri, 09 May 2025 17:55:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a3fb921daa75b1ce5ede793c3821b531f05cc3d0686c381119bf5f5abb3e74`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 10.7 MB (10726931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461e22c3ecb1b5f5de7addbdbcacea5514c98d6d6a2c734d8f9535e5b322b771`  
		Last Modified: Fri, 09 May 2025 17:55:07 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285593a6b05b4824d8be25bef9e5c5a908a816ee7af6139d49b794783fa2801c`  
		Last Modified: Fri, 09 May 2025 17:55:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199382d86c1170c1bbf4396f00d38e7631f7a5109a61903243f116cc7c63482`  
		Last Modified: Fri, 09 May 2025 17:55:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243ee52ed8cd9231a90c3ecfae63ebe080db6ce8a30f54db6d43bb8f147ebbe3`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 17.6 MB (17635411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f9505989c856262190936119cc4430b978ff6703f53b146629679d96b260b`  
		Last Modified: Fri, 09 May 2025 19:02:53 GMT  
		Size: 1.0 MB (1012467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106398096b8676c8177cfb064dd8eede435866da42c16f39a4a63f34a215dbd6`  
		Last Modified: Fri, 09 May 2025 19:02:56 GMT  
		Size: 32.6 MB (32591138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdd449f67a86b211823da1cfeee24e82721c23cf8f69741698c0326b18dd78c`  
		Last Modified: Fri, 09 May 2025 19:02:53 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40fa24f7d3657f775e59d8688dc047b53f23e9b2c6b4ba1c120305f55938904`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb31def92f6e36c2b54685deb2bd3b14d4e1f27c13034fb658c8b0244c9833df`  
		Last Modified: Fri, 09 May 2025 19:02:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6368c952f264ea75b77811cc9a80d1c9d61fa25c271497542a7c1d8b158263af`  
		Last Modified: Fri, 09 May 2025 19:03:01 GMT  
		Size: 59.6 MB (59605098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2a122ea1e68435d5d2f087f1055b88fe4b0a2cb5107883c6ecda659f9b9d13`  
		Last Modified: Fri, 09 May 2025 19:02:55 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1307d0a82e953b93152a9049ea3a472931280ffc623440d8484856c6f1accfb`  
		Last Modified: Fri, 09 May 2025 19:02:55 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:80cc717082d4f82a75faaa11c68e411f424db3019a9a8ba89d45faec89b7d3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 KB (71360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e2c1d9af45a510a8ef495ffd8eae84f2d1da4afb1d3061833480cfc9c18d03`

```dockerfile
```

-	Layers:
	-	`sha256:04337a8f32bed631da12cc700d8ca33e4e87182e6a9e55c4fa084d88676cc754`  
		Last Modified: Fri, 09 May 2025 19:02:51 GMT  
		Size: 71.4 KB (71360 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:ddfa45de90d5793fb51db43119462d04c2a326ce28a7d30d7be642a1c8dc3ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296034896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb987e2a609fb8c99bc840137b88ac4e8e290bf0d80d77440016df28a684b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0826c2c78ee871653d0f57d9c44ce65866504115c48a8494edbe4acb9069b52`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18cc47752cabbb3e0f444ea51014859eeb381a04a9b84e453b349ceeecfef1`  
		Last Modified: Mon, 28 Apr 2025 22:29:46 GMT  
		Size: 103.3 MB (103313187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72914eeea8bb18897afc016693b242383396e76406f7363c6ba1a9be152145bc`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487cf685ebb89da437ccca9553974ef5d8fd1546d00a240c39c8980e18a9075`  
		Last Modified: Mon, 28 Apr 2025 22:34:32 GMT  
		Size: 21.3 MB (21308396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0caf01294aac11114b41679b137bbd5379d9aadc22bcd925f84a08bdb6c5c2`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7c93db4f2696ec7aa86f3d1c0a2db0345e19037a7bb07c48cdf34351262d9`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b00489313302f54bd0d669303a922403cbcc754cfe1dd849c6ea76276c4334`  
		Last Modified: Fri, 09 May 2025 17:35:40 GMT  
		Size: 12.7 MB (12694307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f224f764ec8447f306715a2cd76f19aadd70dbef22b16bd8ea94946ecf66e7f`  
		Last Modified: Fri, 09 May 2025 17:35:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0762824185d358556420360dea3663243ccb60676bf06b265045d8896a0ce3c7`  
		Last Modified: Fri, 09 May 2025 17:35:40 GMT  
		Size: 12.1 MB (12072483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad31017e60189a3fb4896dc1fbb26c66f019e88dacff6bd61827a259215be8`  
		Last Modified: Fri, 09 May 2025 17:35:39 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf41f6797581ca12e0e92cbe2e7531103520deae496a6b556213e1bc39b94d7d`  
		Last Modified: Fri, 09 May 2025 17:35:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a224f5c81b378874f265769dcbf83ef686e896083ef3df2e4a71a74341d18f98`  
		Last Modified: Fri, 09 May 2025 17:35:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8217224589cd89f36faf13aaf8584e82bfe5429e7bcb30f340c777d098d3fd`  
		Last Modified: Fri, 09 May 2025 19:41:20 GMT  
		Size: 18.5 MB (18469592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4431344400fa342df97730ee2be8b9455d74e4ea7f1ccd855931e3f09437bcbb`  
		Last Modified: Fri, 09 May 2025 19:41:19 GMT  
		Size: 1.0 MB (1049731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b68228f2d8cc4b1e8fe6124a1af01700276c01aa9a9c17cb4c0ac0815aaf8f`  
		Last Modified: Fri, 09 May 2025 19:41:20 GMT  
		Size: 35.4 MB (35441903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624045f8a06b800d1ba825dd74e64e17694d0d1f29364266fb9f8121433bb57d`  
		Last Modified: Fri, 09 May 2025 19:41:19 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c517a7ea5d7c15d77850f0d181c3b4b20d91774cdedb127e0139d5e7a2b5fb`  
		Last Modified: Fri, 09 May 2025 19:41:20 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97983b585d3f80fe083926cdb07589095bb836f8347d7c1dfe6f44e79457aed4`  
		Last Modified: Fri, 09 May 2025 19:41:20 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4b2944d7a596da40acab482de9848889b5ccf2eb69be1e046d6c1a55975482`  
		Last Modified: Fri, 09 May 2025 19:41:23 GMT  
		Size: 59.6 MB (59605969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671a9371c561f58270ab44fbabc9acd763f7187e4d6509f665b2907f35b4bc8`  
		Last Modified: Fri, 09 May 2025 19:41:21 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767f0d3d5f000448d1385d45a8cdd71aaf6bb8f0511b10fab1d222ba11d99a7`  
		Last Modified: Fri, 09 May 2025 19:41:21 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:a45cc28410818329453f613e9dde1ee2e40be06d47c101042fa860a2af816db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 KB (71336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d59b6ef231aa89a631a921580f837b88d3be58c9dd8817c2e3779a956b67f7`

```dockerfile
```

-	Layers:
	-	`sha256:50f1bdbae828c0b6799f037c2d586bbb100f389c4e9a8092817574070251c478`  
		Last Modified: Fri, 09 May 2025 19:41:19 GMT  
		Size: 71.3 KB (71336 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:apache` - linux; s390x

```console
$ docker pull friendica@sha256:57995f1c4cbec699efd718442e857dc834fb81c9a9aedd03d119c4680a7e218e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261104773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b234a93b349023c9e7ec572a9195ca9c0040bb966781c08a4907f9cd60e56402`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 23 Apr 2025 16:33:27 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Apr 2025 16:33:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_VERSION=8.3.21
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Apr 2025 16:33:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Apr 2025 16:33:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
WORKDIR /var/www/html
# Wed, 23 Apr 2025 16:33:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/html]
# Wed, 23 Apr 2025 16:33:27 GMT
VOLUME [/var/www/data]
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 23 Apr 2025 16:33:27 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 23 Apr 2025 16:33:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 23 Apr 2025 16:33:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Apr 2025 16:33:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e64042a8c749f17bfb3b660d34f4e07edd06c81899da76f0b866d5592048d`  
		Last Modified: Wed, 21 May 2025 23:40:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae504c4e6cef239a74e8e2bc8e65a5adfc4fd86d2ce43efcb6fcf7b948f38c6`  
		Last Modified: Wed, 21 May 2025 23:40:18 GMT  
		Size: 80.8 MB (80824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9845dffb4e53bff01a8cc52346eef48b2a105a195a30ab820e7df1e9682a7a`  
		Last Modified: Wed, 21 May 2025 23:40:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d076bcc60b618a69a01c7cec130e41e98f5d4ef5c1db46cceb7b121173ee5`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 19.9 MB (19895291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cf1bc43a3bf929df811240c21fd8f7c539c8a225d996960c3345d25963bc4c`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aaa5fa23882a5d77ecfeca856eb346385fec09755a18d670b6ceb0cba14cd0`  
		Last Modified: Wed, 21 May 2025 23:43:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ac3cbb3ee52181f5870c40d6ff0a1b3c15f7a493834b7ffa858d4ba114e83`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 12.7 MB (12693285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5a12f32c7ad22ee862dedc750d697163f4baa8ba216508aec32a28c72eadae`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e519b3f987f99a350906f85a83308a333dc3bb83c855c6f8039d2bbe4fecb42`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 10.9 MB (10877513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f03137a91efb211c66885cb4db54cc38a9ce7daae5ace4b12e9fb71e26971`  
		Last Modified: Wed, 21 May 2025 23:57:29 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5738264205b6a2bb25b89a22c01b95a2a2d35399772e753209307f4344d4a007`  
		Last Modified: Wed, 21 May 2025 23:57:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e03f6ec5d1a9cc5916c74caf43667c2dfcfca33467fb0983bc8c665c61b78b`  
		Last Modified: Wed, 21 May 2025 23:57:30 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8f7f3d4e6323df513d05df476770698c0040c8fbd585c29657f8f3b1574a18`  
		Last Modified: Thu, 22 May 2025 04:55:03 GMT  
		Size: 17.7 MB (17658554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2688993773da07cf94bf14004239e8703086a16472ab8dc1526a5dda84719416`  
		Last Modified: Thu, 22 May 2025 04:55:03 GMT  
		Size: 1.1 MB (1091741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548660ecad5ca1cc995d8cf0785abaa7a4ceba99d2c82beb6ee84782587d3269`  
		Last Modified: Thu, 22 May 2025 04:55:03 GMT  
		Size: 31.6 MB (31567623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe388f0bc06761da1f1f140e8a990976e664e9d412118cec37b2ac35b3c1df4`  
		Last Modified: Thu, 22 May 2025 04:55:03 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea172a1b5a76b30013dffffe0a86a9d7838e258fffb61e0299cd42627597b9c5`  
		Last Modified: Thu, 22 May 2025 04:55:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ec1314844e9360beb8ea65d387097e069e534027caf85dbc4c9a827a66694d`  
		Last Modified: Thu, 22 May 2025 04:55:04 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc86bc10227e92f19d888914edb02814f5dc00338f2bc4f1a6a9d5cc5adf50aa`  
		Last Modified: Thu, 22 May 2025 04:55:05 GMT  
		Size: 59.6 MB (59602427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cfaedfee5f897bb32dfa12c75e79b643e6e9a1df088f90b31f152db9305eb4`  
		Last Modified: Thu, 22 May 2025 04:55:04 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b894f21eaf7014ea5a6f0926996e403ffaee47bbc0cb2de6b80cb1818530e2`  
		Last Modified: Thu, 22 May 2025 04:55:05 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:apache` - unknown; unknown

```console
$ docker pull friendica@sha256:fa72324fb981fc80d744b838c73600e07f5e8aa5742e342c6bd967f2b8481dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 KB (71258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6771e823dba08543358493d1546ceb9fa1726357d0fa70a8c594cca532daa2a7`

```dockerfile
```

-	Layers:
	-	`sha256:21d279a2bc48e8319a802a7c801bf64131c81fe9489eb012e0834d79e4403d72`  
		Last Modified: Thu, 22 May 2025 04:55:02 GMT  
		Size: 71.3 KB (71258 bytes)  
		MIME: application/vnd.in-toto+json
