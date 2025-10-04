## `friendica:rc-apache`

```console
$ docker pull friendica@sha256:fb7e397b033dcd74f9ad085a87f9c2f77a5ed9d0e60003fd214cd8fde2026342
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

### `friendica:rc-apache` - linux; amd64

```console
$ docker pull friendica@sha256:2d41b8727e57cbb6b45f645b85ce8b12eb3c7ba128c5e7d037a2734f38b3aa88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (266000058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ff907bb695d2da2483a081127023cc9c2349653539ce9c1df83f7813b25db0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6026cf2860299a9d9128ea607a676475b53d96921e90b8529e01833526c564`  
		Last Modified: Tue, 30 Sep 2025 03:23:36 GMT  
		Size: 20.5 MB (20466878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038a370b38c8a4d790bd0e176331d9736788470a80254466f0c2ffb9ceccaa7b`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 1.1 MB (1132734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2241b94dfb5421ef5ad2b2f264db14ea6447b82d49616a54d200fe587913751a`  
		Last Modified: Tue, 30 Sep 2025 03:23:42 GMT  
		Size: 49.2 MB (49201272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac94f50df2942f3c58705ac605deb4ad49344350ff2bc6879fbb0a0af62d85ba`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd144b3daeded7659a3108246106ca481aaef0bc8561f865899242d3dac89480`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78713c016d4eaf6e9352826aefd7b606db01460bc3a8e2fab800e923f43b744`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72a28f62eb5f349e12ebe23fc78cdd3b974d8cf769197be340e5a0beefe3a1`  
		Last Modified: Tue, 30 Sep 2025 03:23:30 GMT  
		Size: 18.9 MB (18891405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2003c604c16f08d956efd05cd251e5f7fe1e7dad0c29f301e2e0de206100db9e`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b7c2a63a854b6f89e2577d502bb7b15b65457b24360c4e5bc3d60ab1c6c3b`  
		Last Modified: Tue, 30 Sep 2025 03:23:29 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:33d2846752d3334598426288b4386562a04fe98d04958a3eb103734ebaaf8db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db372eb8cd67aa3e2221a3317c7b6b525eec0f20fefaee4eb0f4829e8ff33892`

```dockerfile
```

-	Layers:
	-	`sha256:695460b8141bce120fb9ad7d5cab00dcdf3d7e8569c6212d3b994f5226a9de42`  
		Last Modified: Wed, 01 Oct 2025 14:28:04 GMT  
		Size: 65.8 KB (65839 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; arm variant v5

```console
$ docker pull friendica@sha256:e90ed78e246c1922ad5fdec6d2508a91b5214378788fd76699d589b858c63c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236080197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de28e012078c69023fd2fed8c030d5169de3b80c1334e92e5e2a4345ee91897d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b007bddf6b8df6f16650adcffe0dacb1fee59c744660556edf359b780192847`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec9f6720c7db6210c9d3b519807d2563820d21df82dfc565b3372ea1a03f61e`  
		Last Modified: Tue, 30 Sep 2025 02:14:17 GMT  
		Size: 94.9 MB (94874060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00daafd9b9ccaf8c1e75baacdf7da67d49b411e9cad365bc72976b3923d0287`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf6a13c90b29503c40921b44fee481f4908ff62c1e04cfcac5e3bf647b1b60`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 4.1 MB (4082004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15942a0743635d309f04baecca177b081a5e5d9ebe10bb8fe45a62cb8eab7ea`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25c7d84a1b4978754571d6ab5d6d6094c1c94fd14c1ef3135fe73b15d27960`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686865f0e335c575c8d11f9d1ca90b1a62fe3feacfb65489ed8e675f880dc93`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 12.7 MB (12744168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4301516f99e0d67bc04ae7a2ed6757d50e1dcf88b63fbfb055f9af8ba3f3060`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fdda99f167dd263c2d6c98893afe00ef998d7e5a121ee771796a0fc00422cb`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 10.6 MB (10591692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d609ba2aadf9efb22d675e38a5396acfd0230df487d1163b9cf508c8e4f16`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408963a86c34aa9abcbf45f7c00a3b246c9e6293104aeed1186ba4614d93dd6c`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c98decf8188290ef713653d29db563f34a629d4dd3135361503821507d7eb`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f52ed47faaa6a14ab8e30cfbb5f0e7e7e8a4a72ad00313a9bb5015be5752bd`  
		Last Modified: Tue, 30 Sep 2025 01:06:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a53baa01f591e4996b73dd2b0c8b676dc742e75e41e9a565f1fd4aa7388cd5`  
		Last Modified: Tue, 30 Sep 2025 02:22:20 GMT  
		Size: 19.8 MB (19791141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a195054a3859d55507cfe00ffd23d55b6c40a6072681f1363650b94f4b0f9`  
		Last Modified: Tue, 30 Sep 2025 02:22:19 GMT  
		Size: 1.1 MB (1107538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f69ba6f26613a218eb0e28adf0013d1f2d1dc809678fbd193c7208aeb5eb7f`  
		Last Modified: Tue, 30 Sep 2025 02:22:22 GMT  
		Size: 46.5 MB (46537073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9612bfaedfd134aca6600e8eba1c1cf25b7269257fcd0743842f3f6760ca6`  
		Last Modified: Tue, 30 Sep 2025 02:22:19 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ab9e1e93a2e5ef5cf809102b3abbd96b954f0ca7e7e800e5ee1ad1df1defd`  
		Last Modified: Tue, 30 Sep 2025 02:22:19 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163201825fb0cdae44be234bfbb73b2e89768800edbb2b24cafdcbde1fc6768d`  
		Last Modified: Tue, 30 Sep 2025 02:22:19 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4235c38699e8dd50dc5e79c6c4f736ee462f144891b47bcbde48517ebb178bd`  
		Last Modified: Tue, 30 Sep 2025 02:22:21 GMT  
		Size: 18.4 MB (18394561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db3ac85d23473f449b48c7d451e863aecbfac01f8dd7d691cdb158407b9829`  
		Last Modified: Tue, 30 Sep 2025 02:22:20 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7544279bbeaf12b8e662b98945e24cc2684d6dccd0a17f5f26d0b6a822c6af61`  
		Last Modified: Tue, 30 Sep 2025 02:22:21 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:c9d4514ef647d58afcb0b9a4251c1d85de466f1b91e081c122568b21f96e7ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abda3dca1d0447a49acf1819ef59cc1c0b0dd77739a46e3ce638817b5e42c27`

```dockerfile
```

-	Layers:
	-	`sha256:3c3a748b552578f5acc748d1125b47be34b8a17a2935db49cc74ca96eb558286`  
		Last Modified: Tue, 30 Sep 2025 08:28:09 GMT  
		Size: 66.0 KB (65987 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:e022f1ab6702792ba83d620bdf332905fdafe18e365dccd4564215eb4b24323e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222968575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f963b554aedf43d94d00b895f83bce3a53d9984a798d53eafc3b3e27840f9d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce819c84fdcc6e61bb091589a0b208d02d460713f8dbe4d17ff7e33a36f900d9`  
		Last Modified: Tue, 30 Sep 2025 00:06:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f2a554c44d6e229aa4e66a678289311feba8e355071ceb877bbebeddfc4bf9`  
		Last Modified: Tue, 30 Sep 2025 00:06:29 GMT  
		Size: 86.2 MB (86245392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c1c85f1cb509addb65cfaa888cc0ee1cc9464030eed921f79f86b26ae2612`  
		Last Modified: Tue, 30 Sep 2025 00:06:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fed3ef3e48e7f4952008092af4d10c443bbb5272361bd071535c4f5a289d955`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 3.8 MB (3752006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b2a3b75024af9d062e6d0fc7eb4d0d02310f1e625b06eb5d3dede683d6518`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99235e87a669e6d891f9f1b299fe4d372a22ceb8d3580bcd8db9b751897b7c6c`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99c8a4b51961d491c0388bcee9534cc4f9fb3e5b48bdf0164ca427bf3b6dc9d`  
		Last Modified: Tue, 30 Sep 2025 00:17:26 GMT  
		Size: 12.7 MB (12744364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da3b510312fdd1495f4f325dcc9d60b71710735c9d1b16ec6046105cc2afcf0`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615652fa79960d0a851d122ed8d0dacecc33ea955d26a2763f9c735aadf30ab7`  
		Last Modified: Tue, 30 Sep 2025 00:17:27 GMT  
		Size: 10.1 MB (10064437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede3576e182c2759883e5d781b08b94eef40e79d722f48e51742d2c6ea3fa1c1`  
		Last Modified: Tue, 30 Sep 2025 00:17:20 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371235052af5ee8f742744b99ee6b4665c8cccde64df8694cc4d1ebec1037038`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875d4eaf0bebe7a1fc26cf60b4073d4f97ad5a7aaeadb18e7ee1a851ffd7ce02`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd50e3c95c94cc549fe2c9eaedfd9eda8f83864681d58e09edebd1fbb54ce9b`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb10185f3fbdfd733656d87f8dad9dfd5db5c6ac6f373284b08c9bf584b185f`  
		Last Modified: Tue, 30 Sep 2025 02:47:12 GMT  
		Size: 19.7 MB (19681285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32f800a91c8faa1e1321a16a034af1fe27e70199524b52123da686ce03260`  
		Last Modified: Tue, 30 Sep 2025 02:47:07 GMT  
		Size: 1.1 MB (1097973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed915b499eb3a56571ae49a6f103e1a85f87f2ca4ed7c2aab8a584c462299a`  
		Last Modified: Tue, 30 Sep 2025 02:47:07 GMT  
		Size: 44.8 MB (44798476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beecfa6df74a29a8a7bcd3654f798938790747796e25062058be8941a4bc2a94`  
		Last Modified: Tue, 30 Sep 2025 02:47:03 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becfa2cb5bfd513d4460158abcab86da744a9bde87cb1175d95df364e8479b0d`  
		Last Modified: Tue, 30 Sep 2025 02:47:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d366c4cb5b03abf3db51583d6ec50c2de6ff5c62b8cce84fc7f5fd16a7033e`  
		Last Modified: Tue, 30 Sep 2025 02:47:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8627df82c3f471de70447916aae974b5afa942f789e43693d075ab4aea831ae`  
		Last Modified: Tue, 30 Sep 2025 02:47:04 GMT  
		Size: 18.4 MB (18360046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15974c34f07f84d2737f25ccc1f6bb8a057c3e45b251bcd06dca4f742a6fa95b`  
		Last Modified: Tue, 30 Sep 2025 02:47:03 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0702e3590086e0f14f9ac2da1e8408134dc709419776931e8d51f86ce5cc068f`  
		Last Modified: Tue, 30 Sep 2025 02:47:03 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:856524aac38fc9b7be327a6085e69fbcb6eb9fcdbd5ca923fd3aa7abe857c246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c3ef73fe62d7f7370b8afe22f37d1685ca9ca136b6b58a512118bd117bf193`

```dockerfile
```

-	Layers:
	-	`sha256:f939b950c942b762100c21176a07256e954c319b2efaf831504d68dc27c2a3b6`  
		Last Modified: Wed, 01 Oct 2025 20:30:17 GMT  
		Size: 66.0 KB (65987 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:5dd3847bb7311fd34a00f899b912e51981d2ef8a5a21dca0fe4171a68f1ea506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257451724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9031e961f18c01131031d52887c01b65b954fba74bdc656283e5ec30607a02`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619104e285c4f7650532e48f53659936c4e3e785f4f9e74fdf3ebfaf8f3030cc`  
		Last Modified: Tue, 30 Sep 2025 01:08:32 GMT  
		Size: 20.2 MB (20199036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b74a6434ef9e06c617ee83de1f5fbc84cfed0bff907c627874c4ad4cc8e682`  
		Last Modified: Tue, 30 Sep 2025 01:08:34 GMT  
		Size: 1.1 MB (1064807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b6a0d213d409116ff7ade18b2e32c9f836bce84a86f25d7142c833905a9b2`  
		Last Modified: Tue, 30 Sep 2025 01:08:36 GMT  
		Size: 48.3 MB (48336438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6507cd52967e5b66bd863e439ece5d0194969f35f1695e0fa895447be6d271c4`  
		Last Modified: Tue, 30 Sep 2025 01:08:34 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d407c56d6ac7d33583d4bf1c0ba43b2dae25c2b9dc77d616e2f806bc925ebf`  
		Last Modified: Tue, 30 Sep 2025 01:08:34 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e70b25801787b59ef3083c8961741bc4519b37f3ee5f52aa0f720b1baadb2f`  
		Last Modified: Tue, 30 Sep 2025 01:08:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8d4ff08defd5fb1fd7652c4602086d69a6ba2c9892caaa0a721beecf19b8c4`  
		Last Modified: Tue, 30 Sep 2025 01:08:37 GMT  
		Size: 18.8 MB (18755458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967f870171138ac2dcd8dd7d803ff5caf512ac87b2ecc2ec3663d38176a91e1`  
		Last Modified: Tue, 30 Sep 2025 01:08:36 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a3503bfe7072d7f49603d4b96214a01bac3abeb945ea77a18c8b6c65d9ee36`  
		Last Modified: Tue, 30 Sep 2025 01:08:36 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:54ce06194a5c08f231bbcfab41671fd26c5488ad991edfbf9d99c568fff47bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (66033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b20b88aec80b3bdaa5bc7f468571e9ec15bf8b0bec3d2c90300374a5d7672c7`

```dockerfile
```

-	Layers:
	-	`sha256:f67b4292f3642d88e6623194916202d80eca9704ab6940fec9421764267373eb`  
		Last Modified: Wed, 01 Oct 2025 20:30:20 GMT  
		Size: 66.0 KB (66033 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; 386

```console
$ docker pull friendica@sha256:1d4ab76b0fb352d89f2956c0335cee5b8c59a57ee854ab4528290ce633b5b3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267094319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723c24098501692f8c1dfc15f049ba0c2182e1cb69e62390fa65251d5febbd97`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461ff14037e9e86052111a11f5d19afebb2bde96140c152cd47a51979184a55`  
		Last Modified: Mon, 29 Sep 2025 23:59:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e047cbcbd0717bb1b9fdee77e059658d262320e1825b77027d09be649095e242`  
		Last Modified: Mon, 29 Sep 2025 23:59:34 GMT  
		Size: 116.1 MB (116138188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408c02c3bb09142f028ad0ace874d7d7c54e899cb939a467ec76886730f8f27`  
		Last Modified: Mon, 29 Sep 2025 23:59:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606c239cf33fabf307f998a4e2fc9480a0d231edf41ad4dd748ded819b895dc`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 4.5 MB (4455463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2639cfa6bfdb3e681f4583b1b86d72d112539e52cb432ccc0499c3177a23c7f`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eaf83312b44093e6ea71d00412083eb1143122878954ef3e552c8d643d0c8e`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc0fb7e819ad24f48de136ffaafd38d0355c58414351fad1bdc9b2811a3e828`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 12.7 MB (12745631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b136f66c4fa025bcb6a67e4a7aefe412b00b8a1ddebafb965f2e63a86f83c7`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e82924a158381d19f6dc867fb0196ce0b10b8d977d7d10575a1306920be159`  
		Last Modified: Tue, 30 Sep 2025 00:03:03 GMT  
		Size: 11.9 MB (11917023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ab55cd62bb1fba68c5ee47e142cc1fac4ded15c96cce866cc62cdf6517864d`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd311e28774a48264de7a45fcc2871b00c681707f06033156062f33f820238`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917849e8458de58339fc3ae90b713cad4f232b8eddc1521015aad80863f7ff77`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf5cf0346847a23eb573c07f9243fa8c3570c7c3a4c172734de39e9ffa9778`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815699a6604832d0451b46b73049fc913ab96c10ac734509bdb651b6c02bbea6`  
		Last Modified: Wed, 01 Oct 2025 20:30:52 GMT  
		Size: 20.7 MB (20703663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f6bbfc4ce93335cc27c159dbee1e4ec52113df0354fff19277c1e20c7cee9`  
		Last Modified: Tue, 30 Sep 2025 01:52:58 GMT  
		Size: 1.1 MB (1107446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca5d7ab6c988e735e520a8b3df69cb5955fdc427a790dce97af67a941f329d`  
		Last Modified: Wed, 01 Oct 2025 20:30:55 GMT  
		Size: 49.5 MB (49450806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59018f7048031089b5e22371070c2191a6a7bffafcd8e1cb0a2fe027643f0a3f`  
		Last Modified: Tue, 30 Sep 2025 01:52:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e2e461515ea06723e1f65c7ea6407c007b5a5ad8c2f0ae7ca858118eb8a4d`  
		Last Modified: Tue, 30 Sep 2025 01:52:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a188b28f3910335ec36307c4fd43cb0ac63777210b4c9d0a5dbf614f511f5`  
		Last Modified: Tue, 30 Sep 2025 01:52:58 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1762178bef708fb9c491d7bf401144d70b555d7724de6fe50709f6768b373033`  
		Last Modified: Wed, 01 Oct 2025 20:30:54 GMT  
		Size: 19.3 MB (19269731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41701f7ca031631fbc7d66bb6d9826491a7cb69d615f0c718744a1caabf9f55`  
		Last Modified: Tue, 30 Sep 2025 01:52:57 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d1b3d3ae1aec9792fb178b00072c0996cf09bad39379cd0a315ea4b6a8c0ac`  
		Last Modified: Tue, 30 Sep 2025 01:52:58 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:430f31a47e11c07f6e9ac83528aaab6ac93d675eba0a4c6794c1c6952efbed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a745accc0c9ec233d1013d5de6b26e4763d23ee06e9b62a1be1fbd798526721`

```dockerfile
```

-	Layers:
	-	`sha256:89d7645b7294ee5d636e019f41ba8cf3b511b428ceadbba7241c15f5cfa6f329`  
		Last Modified: Wed, 01 Oct 2025 20:30:23 GMT  
		Size: 65.8 KB (65795 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; ppc64le

```console
$ docker pull friendica@sha256:6145d12702c285ee45db4eb2bbb22fd3fe37f34421c3266fb0c955c404092ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264444860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64cf5443839dbdcf9c9f9a267f874f03f4eee332db2b95bf2e4d4a1d8c76420a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8f05f06dc824d87111df6e83c98b44d4b30120744017674fa115b47c2dbe6`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75015a3f4b08f0357c989a4c27950c8a6de956a67874e0df0e8876482f1c6285`  
		Last Modified: Tue, 30 Sep 2025 07:16:10 GMT  
		Size: 109.6 MB (109597733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbf93152fe00ebb17d96bb0b9dce5763e9ee0f645695274ef06bcf783421bd`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdaf3986afeff98ab8e26d5054958a0fddcd91c28e37dfca6c9bd1937c38c1`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 4.9 MB (4875653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd3405d5eef9a007a25174bf4a788fce2a6cb8f4d2a07d35b2433b2d1d52fb3`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0d88f08b4ee89f9ccb3d82e7e8a74e3a33d00089433c4500c8c0bf24c522e9`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77edc343c916403763589f847c954cb7307d1ce3a5ddd81949086c26a528303`  
		Last Modified: Tue, 30 Sep 2025 07:58:17 GMT  
		Size: 12.7 MB (12745895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e900f713a9f47d326b39e139b7d0e403be4974d90260ca685f97fd170c0318`  
		Last Modified: Tue, 30 Sep 2025 07:58:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b873839233b2b57c86a027faf3ceb57b066bd95e5ecdd25e85ae6ed114089cf`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 12.1 MB (12116907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055d60b33f5e4a67049ceb0ec372674ade80bd1fcaa40a4d1cba22e7328173a`  
		Last Modified: Tue, 30 Sep 2025 07:58:15 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5520a113744694808a200592d73e60ac4e0b161e0574d6e20ced25649fffcf`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9265b962f01c977332d57f7f8969ae776bda0156ff44343163bef8a1327019a`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cca64b19960a3ef677a3543ffed63c42782da3b2b81b0594e8c8c286911710`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e08097b95cec5a568da2cd1bd40f3087852a5b999b814bb0eaaa865ea9f515`  
		Last Modified: Tue, 30 Sep 2025 19:40:22 GMT  
		Size: 20.7 MB (20651784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c7345932bfd02599e558cdf4fbf6649253c66464593c19ce1d69323d44ccc`  
		Last Modified: Tue, 30 Sep 2025 19:40:21 GMT  
		Size: 1.1 MB (1054783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3bff720a809c8352d23a5a857a6ea7de8ce4c85dae7177d5727a5c4091a5bb`  
		Last Modified: Tue, 30 Sep 2025 19:40:27 GMT  
		Size: 50.8 MB (50786137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdea7832ee9f926d0ff7845f26d5140573f2623bc3c4dfe85ed59c562af6d4d`  
		Last Modified: Tue, 30 Sep 2025 19:40:21 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2273f6fec54751ff4868ca41c6cadd9fb864900296219aaa500e0013a0a490`  
		Last Modified: Tue, 30 Sep 2025 19:40:21 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6732b643ef89745a9c6876c489c9dbb792fb54660a27a3ac39d1f79aa221ee65`  
		Last Modified: Tue, 30 Sep 2025 19:40:22 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2cf1dcd02b95f901030377cbd732087e796c268ad0d6fefb0ab49f12b39bbd`  
		Last Modified: Tue, 30 Sep 2025 19:40:23 GMT  
		Size: 19.0 MB (19005678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68d3f2e646fc25171585d0ac5f7f3ba15e8420dc3a4a1942662c70ef1510ef`  
		Last Modified: Tue, 30 Sep 2025 19:40:22 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe730cc5d2850f4fe24febabf6054ed472c21c027207a1d90d1c4d2c1c17dc72`  
		Last Modified: Tue, 30 Sep 2025 19:40:22 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:d793655b62ef5b2823dcea84dbbbac3631ca80c257340d0f82ff1e0a6970efed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442b1831017b299660157a0a695c974bc2903f8d6d517e5db9610339146eb916`

```dockerfile
```

-	Layers:
	-	`sha256:c51a248750e2396b2a8646425ce74ad6f84b0ffe1037e488611cd1a2823ea815`  
		Last Modified: Wed, 01 Oct 2025 20:30:26 GMT  
		Size: 65.9 KB (65895 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; riscv64

```console
$ docker pull friendica@sha256:b3c496664b2fb6c8b8fd132ba5463617f379ae440303f4a7a12dc7a3da80eb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301659054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ea77176fec4d81010e38230a43d8c03c838f6c56e3e554c349a5d4aefaaa00`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10c25f1d43bda19fe1addca79e55bd60680b6683c485853db1be0763dd7e2`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03438fb8247e71c15afcd0508b678af32b8a41a4cd64dda788e8224b32557902`  
		Last Modified: Tue, 30 Sep 2025 15:10:17 GMT  
		Size: 146.6 MB (146579364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df117f051d654fe662d0af341155be2d955517920079566410cd20daddb0a237`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820c12643e6a3e49d793483aa7a8f0fc043801a3e3d7085a78a2243ac2efa0b`  
		Last Modified: Tue, 30 Sep 2025 06:10:09 GMT  
		Size: 4.0 MB (4026042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13195b106bcebf839d7af0f2269c2a442a10e9e41e345d562397fa27f3d35f90`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627b6eeabd2d7dec5e31e065537160dea1d3126b8ca00665c8bbb2aaace9b070`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fe47ae8b684f5caeb83d9cd67cf89fdf0fc2383d69dbbac08c501112421d9d`  
		Last Modified: Tue, 30 Sep 2025 13:56:17 GMT  
		Size: 12.8 MB (12760793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9facf10beb33f09907f6b28f68613d3c5682c3f7151f216c385f6b0cedb93bb`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80438ff315a32555c89c6a436108b19441c75de91f63e5823891962a8f82816`  
		Last Modified: Tue, 30 Sep 2025 13:56:17 GMT  
		Size: 11.2 MB (11247976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f213298c7495f6f0834e5d36e2cedbe5ad94734747b1198e341a8662caeeea`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff4b32a0686b241a5f4d73f6b49f274047ec58fbce1293bb869c960995bf5e`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c424c4b576c259db3f48b1e583c6c162559f9c547b2455e798a14f97ec49586`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8768d29dbe1389096ac1264e963a24cda78ed7f1a04ded93bcf27ba00553da07`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e13bd9b7ab9ea54c43c8964cc19cb0293b4328d48e131ab0b92e4ef7ace82`  
		Last Modified: Sat, 04 Oct 2025 05:03:00 GMT  
		Size: 19.9 MB (19868380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7156e3d97a37a71ff303e504f824136fb4695012d2c40951765ac9b4a4f9b8b`  
		Last Modified: Sat, 04 Oct 2025 05:03:00 GMT  
		Size: 1.1 MB (1103230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33e72b41947a1c1d5a6578854eb23ae8f42f5484b940f1a411a8d12d8a1f681`  
		Last Modified: Sat, 04 Oct 2025 05:03:03 GMT  
		Size: 59.4 MB (59444603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37b74ee778cd3ff96f8d16443108b212578d1c2ca5715b5e932a7a7e55a3edf`  
		Last Modified: Sat, 04 Oct 2025 05:03:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6514ab86389d1650a2acf14ce46b35e87c01d3a0c30792c698afc30dd5ed42`  
		Last Modified: Sat, 04 Oct 2025 05:02:59 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70a05fd668402387e9ee526b9102484c192763e0f7737d81355fafdc7cfbb0a`  
		Last Modified: Sat, 04 Oct 2025 05:02:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9827e41a047a90b809038fc0adebc2148eb259532ed888e09d5e440f8df5cc2e`  
		Last Modified: Sat, 04 Oct 2025 05:03:01 GMT  
		Size: 18.3 MB (18341291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43992da64ff2e4470c0c027a3cab53c804a14bffa2c23c6d221edfb4af32bb4`  
		Last Modified: Sat, 04 Oct 2025 05:02:59 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469a270c3bd34148b6b4f5768d16acd360b708def17ff7cbba32f57251eab86`  
		Last Modified: Sat, 04 Oct 2025 05:02:59 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:ac4c2472113969af700881ae70c648c8140f78952f805cb28da77e11152ff294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361843850d3c90dc72bcf2c5fb8e51512d0a663454ef91aaeb9dd34f9ac5eade`

```dockerfile
```

-	Layers:
	-	`sha256:7c160b3dee14a8169635f2d6dfeebbb108d8c02329c1aceaf93cce63d2872e9c`  
		Last Modified: Sat, 04 Oct 2025 05:27:46 GMT  
		Size: 65.9 KB (65895 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-apache` - linux; s390x

```console
$ docker pull friendica@sha256:71a52f9704555e13583a38543196b7630c7b299f3a0779bb24a73f27d8f3fd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238396504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680164db74f3fc7cfed110bfec8fccddf578e09a689a751959b6c8f8474c2eb8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 30 Aug 2025 22:12:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_VERSION=8.3.26
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 30 Aug 2025 22:12:39 GMT
STOPSIGNAL SIGWINCH
# Sat, 30 Aug 2025 22:12:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
WORKDIR /var/www/html
# Sat, 30 Aug 2025 22:12:39 GMT
EXPOSE map[80/tcp:{}]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV GOSU_VERSION=1.17
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/html]
# Sat, 30 Aug 2025 22:12:39 GMT
VOLUME [/var/www/data]
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sat, 30 Aug 2025 22:12:39 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sat, 30 Aug 2025 22:12:39 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 30 Aug 2025 22:12:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9ee178226f7ea0f482af09b7dc3ba5fca7c07de96e60ad828b1737709e6b19`  
		Last Modified: Tue, 30 Sep 2025 06:40:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b8c6f589e7cb0b9aff90a6df6a7cccfae60ed23d9fc4328b15d0c44aa0266e`  
		Last Modified: Tue, 30 Sep 2025 06:40:25 GMT  
		Size: 92.6 MB (92564454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674ff7c7e8a7de8708af6056d40b56dffeb3ae246f618226bf482e0f207ff014`  
		Last Modified: Tue, 30 Sep 2025 06:40:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a4110d360212ee6e0ff8a1ea6d731b2aaff510a71163b8a748a26aa60e590`  
		Last Modified: Tue, 30 Sep 2025 06:44:29 GMT  
		Size: 4.3 MB (4320480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763509a8474369ab3c7c1528f033ff966ec368402debfbc88d137b2f4ab19403`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d5e9b63e43b1a0a70264c4610e6f5dd857a8d5245e08b172e026ecb396e1a`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b259324a65e330e9f681f2e5950782f713b110e2c10f3e934bc47fba2ea0547`  
		Last Modified: Tue, 30 Sep 2025 07:17:16 GMT  
		Size: 12.7 MB (12745179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5834b2d85fe4a101cfbaae2ec80c35f43d1e594bc2293aed80a7db76d728c6f`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9b48987db0e93fe5b9be24c82dbc5be2514ebe7a66969ee6803bafe88c25e`  
		Last Modified: Tue, 30 Sep 2025 07:17:17 GMT  
		Size: 11.6 MB (11562688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73636a81b76033d489c97758e9dc4c95e764ed93efef24e9b994f4cea791bbf`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82e61548fe1c152e7c3145740867ca12096eb1ee3e589a8e098707eea008d9`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4577b80535eb680a848be96af4451818cedcad81c4842724f7b7ae3f13179453`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410955c39f3e9374ffd55640d3f06a79d6408368f4bab4423a5f6630d5adde5a`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b95e1f9a3d17622ec1ff59eceed216618501667e1897a8eae0c2e80a71ffcf`  
		Last Modified: Wed, 01 Oct 2025 20:30:51 GMT  
		Size: 19.7 MB (19749836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb5bc50a44f44abee51093abeab9763021bc54d2e4d733b8cfa9c2ee7759b5c`  
		Last Modified: Tue, 30 Sep 2025 17:17:20 GMT  
		Size: 1.1 MB (1097293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f345d190c3448c4f69e2f564adf898d911f76dfc1d4a60650e1f3cc4fe8f0`  
		Last Modified: Wed, 01 Oct 2025 20:30:54 GMT  
		Size: 48.2 MB (48216665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dde7f56f7cf2aab80b744ff10a8d3d081f434f908659df1130662a830b16da`  
		Last Modified: Tue, 30 Sep 2025 17:17:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e862b1fadde597d930bf925208461ffa042ae4011f709cd43d983efc169105c0`  
		Last Modified: Tue, 30 Sep 2025 17:17:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c472a2acc4e5f2ac8047eb73c031b8f0bf2395cb388c395dd4512c7391efaa0`  
		Last Modified: Tue, 30 Sep 2025 17:17:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a14c5b76dded6100ee0a800b2b10610abd7eb1920f07029b606f95cca484f19`  
		Last Modified: Wed, 01 Oct 2025 20:30:59 GMT  
		Size: 18.3 MB (18290856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bdfcfebfbd8e50d0b36593bbd8dccd0a91ae3c3629e612932f752052811a49`  
		Last Modified: Tue, 30 Sep 2025 17:17:23 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc707b1a27c6125141527ba6eccbc84186f50a224f1b230185501131860923b`  
		Last Modified: Tue, 30 Sep 2025 17:17:20 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:020f97dc864eb0f593b4f66894121dae7c1f237f77a4c1893d5e0e3c3e558fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b3b51e382bbc26c8c6901071af26c86eec454440c031efff3d8d391cf02312`

```dockerfile
```

-	Layers:
	-	`sha256:281725aa4efd35af7ed546a987eba2acbe045d91c1be8da69b493a58ba2c34aa`  
		Last Modified: Wed, 01 Oct 2025 20:30:31 GMT  
		Size: 65.8 KB (65828 bytes)  
		MIME: application/vnd.in-toto+json
