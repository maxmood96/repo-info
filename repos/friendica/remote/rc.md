## `friendica:rc`

```console
$ docker pull friendica@sha256:0ee206e422840ad9fa9f6ab763a83eab6e044faae3b48087c34ac663df2a560c
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

### `friendica:rc` - linux; amd64

```console
$ docker pull friendica@sha256:d2c52162da342cd04fbbaac14a87e7d5ee5fab8898508bb9143de39df6702dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266074443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b8be603c9ebc3984fbf5ab946318291fa9f9f30ee9911f94d40e0f1b421a41`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:08:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 04:09:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 04:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:09:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 04:09:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 04:09:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 04:09:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 04:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 04:09:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 04:09:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 04:09:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 04:09:12 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 04:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 04:09:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:12:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 04:12:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:12:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 04:12:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 04:12:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 04:12:01 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 04:12:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:12:01 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 04:12:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 04:12:01 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 07:44:06 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 07:44:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 07:44:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 07:46:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:46:56 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 07:46:56 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 07:46:56 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 07:46:56 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 07:46:56 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 07:46:56 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 07:46:56 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 07:46:56 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 07:46:56 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 07:46:56 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 07:47:01 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 07:47:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 07:47:01 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 07:47:01 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 07:47:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25196dda40f759cd150442f0f6c3cf759c3231c93e9d860a3cba9a4f0de24ca`  
		Last Modified: Tue, 04 Nov 2025 04:12:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a827a0ac463346584970fed0fc164837e239a954717661a6c17b289e7b62f`  
		Last Modified: Tue, 04 Nov 2025 04:12:47 GMT  
		Size: 117.8 MB (117838099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbab8e237a8338cc63f169b55bcad704a1af2104ae71c54fdcb009ea38685bc9`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9661b3aaacf221bb4e05988bf62f457b61fbc6bd1b9a4f8e159d5a02c65dc9b`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 4.2 MB (4224045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5d8c5c0a78943de1f3d89e9b90dc37883f292542715688c7754c430dee7d6a`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf0c79e6afebb574965ffee3239dc119adb4486efbbe3d9b4f3c22f890fb57d`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cd6a96a8baafa8cc61ebeaa2885f7d3776d5bc8c4d99066fdb357697adad83`  
		Last Modified: Tue, 04 Nov 2025 04:12:34 GMT  
		Size: 12.8 MB (12757968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c855dc7e6b444a530bed318438a72d94cfd67d52a4a0fc257357cc252bc4a`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd7dfb6bac9cb53ee854dd08854706fbaa5f55da39047cfecfc67afacfa7dd`  
		Last Modified: Tue, 04 Nov 2025 04:12:34 GMT  
		Size: 11.7 MB (11711701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5d8cfffc0dd832b5b71e688dc6aeb8630380d641f3e15fce1d8e6de57f361f`  
		Last Modified: Tue, 04 Nov 2025 04:12:33 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744bf4de2f14cf170c6557591de263ab85837825bf7b5c88840d0622c642f234`  
		Last Modified: Tue, 04 Nov 2025 04:12:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07405ca45eb7e0c355bc18e25719f083d61ee71506762b23ab13f2cc25ca2088`  
		Last Modified: Tue, 04 Nov 2025 04:12:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600eef74f4fc075f0e250529f4044dc2771ee5f79090f0648b38cef05fbc68b8`  
		Last Modified: Tue, 04 Nov 2025 04:12:32 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76890fdbac2259c33f4e284450803c3a2d2b4e751dd4c62f02c2eb5aa026139b`  
		Last Modified: Tue, 04 Nov 2025 07:47:22 GMT  
		Size: 20.5 MB (20491702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a963a7b81f67cc7a75d9acbf57f8dd128e142f122b15aa621c86a71d3302eeee`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 1.1 MB (1132604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c630c20bdae63fe852a0f060cb7aa9349b41b37ae62145170d224fa0102ff338`  
		Last Modified: Tue, 04 Nov 2025 07:47:29 GMT  
		Size: 49.2 MB (49202121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108fe97a9e5ef857658c2ec132d725232cc1c81e5fae4930dcb4b012fa4f3a8`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e0afff0d7d0330247281f363f6c14aa3388083a29a3ef0b4a1f9888133cd4`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cf2b256841f22b4a94f9e9b158cefb10dba376b49c45b5503b5b20455d9c33`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193d505c37e7cc3766a8650903c4b0a8cfafa14f9edfc7b41a2ad151049ac4d`  
		Last Modified: Tue, 04 Nov 2025 07:47:21 GMT  
		Size: 18.9 MB (18926418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb26578d2f44ac15435fd4a064b0318873bde115037b0e57320e621566cfb66`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6871303da89dca235e49a6cf9032445d495b8eb2b14c9834ce580c884a69ff9`  
		Last Modified: Tue, 04 Nov 2025 07:47:19 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:7f1de4c50dd80eae7f54e1442f478fcf5b245bf406da9c7f10ac4691860f09a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd73a04de08e4f03961befa1442f80fb90c46eb2d07b49939f9eff3bc8a4e13`

```dockerfile
```

-	Layers:
	-	`sha256:65dce6288f0fa8f4a2c0f7495a7ee38a118c4a9ac3e16ecb25011588999e45e1`  
		Last Modified: Tue, 04 Nov 2025 09:28:33 GMT  
		Size: 65.8 KB (65796 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm variant v5

```console
$ docker pull friendica@sha256:99a56af6ed083a045d95e07f5e5c23017891f53c56c44e288bcb39fd54c8469a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236175441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e9d5319bc4093087f9087811d2ff0f364dccfd1fdb98da9920131fa67281a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:29:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:29:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:29:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 00:29:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:29:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:29:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:29:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:30:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:30:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:30:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:30:05 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 00:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:42:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:45:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:45:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:45:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:45:34 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:45:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:45:34 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:45:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:45:34 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 02:51:58 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 02:52:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 02:52:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:55:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:55:35 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 02:55:35 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 02:55:35 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 02:55:35 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 02:55:36 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 02:55:36 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 02:55:36 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 02:55:36 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 02:55:36 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 02:55:36 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 02:55:44 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 02:55:44 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 02:55:44 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 02:55:44 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 02:55:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2e4c06d1bc9814b559ed2d88091bd05b3b360ca70c0c1e7204ce6190f55ef`  
		Last Modified: Tue, 04 Nov 2025 00:34:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d089a1b535ef3993d30b2d647446b4afa32a26d5413a75d152b59fe99ea9f`  
		Last Modified: Tue, 04 Nov 2025 00:34:39 GMT  
		Size: 94.9 MB (94875678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469637e1c3bb6a585147af3af7cbfc349d954b41614a7b6e39d0b2d80fb9739`  
		Last Modified: Tue, 04 Nov 2025 00:34:26 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81423a9eaa187174e3c82e3c4a29e5018b0a9875574e89ebd73135724b79057d`  
		Last Modified: Tue, 04 Nov 2025 00:34:29 GMT  
		Size: 4.1 MB (4081966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cda78148ca5286add421d1f7e2ddbdb60fe81e5bbae12dacc1e934f85a2cea`  
		Last Modified: Tue, 04 Nov 2025 00:34:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324a6b46a43e21ca92f9ea0ecba8f5891358fa271e5e49f963aad7e90ca1c3f6`  
		Last Modified: Tue, 04 Nov 2025 00:34:26 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05be0b5f3714fa335f332e047cbc7e6894828c6b8f77bfb8b004e2d90ff70add`  
		Last Modified: Tue, 04 Nov 2025 00:45:55 GMT  
		Size: 12.8 MB (12755522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb5573c1265929833ff61b3b1b716b6d7b87aece23baae67dce411214fe210e`  
		Last Modified: Tue, 04 Nov 2025 00:45:52 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c14eba0a874c3d150205b26325972cfb3ef4abffab722a8200eb9f81f27988`  
		Last Modified: Tue, 04 Nov 2025 00:45:53 GMT  
		Size: 10.6 MB (10595120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f499fec74e735a18e82e70fb8bb6772d102b1c57a0759fc7d990734a909d8f4`  
		Last Modified: Tue, 04 Nov 2025 00:45:52 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c75d80acb3b23c1efd1649aa64890d95bca269c5f24be3714be1f9261f1478`  
		Last Modified: Tue, 04 Nov 2025 00:45:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b34a5b67f8cb6488cfb15005988a818213244487180fcf0ee8f05b9f2bd30c`  
		Last Modified: Tue, 04 Nov 2025 00:45:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c24db1d9d7da1c46e4f3eeec2e6adc1ab9ef37ca85207b1de846b2fbadb8b`  
		Last Modified: Tue, 04 Nov 2025 00:45:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ee435913a39616dc19e64ddbef041043485ca1a515c54810ddfbe27111c5a`  
		Last Modified: Tue, 04 Nov 2025 02:56:01 GMT  
		Size: 19.8 MB (19834544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49e7965f6825df0dff87d21df6af3c419ca64f10ff426efa461842e5308c5`  
		Last Modified: Tue, 04 Nov 2025 02:55:59 GMT  
		Size: 1.1 MB (1107495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c25da57b3862d78acf482e6d09be54baf5d22ad5d0424e6ba668b8a31bf92f`  
		Last Modified: Tue, 04 Nov 2025 02:56:07 GMT  
		Size: 46.5 MB (46536915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8535733f616ef14b310bccebfc3b3c28dff7943c610007ecb1857c9bbae16dec`  
		Last Modified: Tue, 04 Nov 2025 02:56:01 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297fde409bfdd500f4549cfb3a262833ccc6ecd3ac84e99e03725c613940b4fe`  
		Last Modified: Tue, 04 Nov 2025 02:55:59 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93bfb99bad0ca017ec947c268c0562dc8eeaa93b46238cfd6208958360959d`  
		Last Modified: Tue, 04 Nov 2025 02:55:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33b1f6593eb18d60402d7296f35c526284c03eefccf318d3ecb8d931a101ebd`  
		Last Modified: Tue, 04 Nov 2025 02:56:00 GMT  
		Size: 18.4 MB (18430081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa855f0bbb4299d7fe5b0ec0442a8a600f0024083bd170c8346696d4ebca9a1`  
		Last Modified: Tue, 04 Nov 2025 02:55:59 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b793f4969f6d074fa4bd99b32c2eeee1a69b7ee4ea7939f935004cb50dcbe4d8`  
		Last Modified: Tue, 04 Nov 2025 02:55:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:c4ffbe9527669b05ee54a602912891048308272298666fb8edc9e9e368247785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a20eb88577f8eb9e827dcb4a50ac91a4f059e1bd7fe091423ad24912db25817`

```dockerfile
```

-	Layers:
	-	`sha256:3d37ae540d7c87196e9e26d46250cdf92a4ca0d030bc95bc649e2db60b7282a9`  
		Last Modified: Tue, 04 Nov 2025 09:28:36 GMT  
		Size: 65.9 KB (65944 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm variant v7

```console
$ docker pull friendica@sha256:51f43e56d1d94a650d6541bad1a8a95ed30d5eb75a7f45774ac4c580196f71ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223061242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b35a83d8edcf7fcc5f2bf382009781fcec3b1da7dd9121d5fd21202d99ae34`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:07:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:07:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:07:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:07:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:07:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:07:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 02:07:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 02:11:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 02:11:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 02:11:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:11:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 02:11:21 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 02:11:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 02:11:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 02:14:10 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 02:14:10 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:14:10 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 02:14:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 02:14:10 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 03:23:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 03:23:12 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 03:23:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 03:26:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:26:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 03:26:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 03:26:17 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 03:26:17 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 03:26:17 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 03:26:17 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 03:26:17 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 03:26:17 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 03:26:17 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 03:26:17 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 03:26:23 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 03:26:23 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 03:26:23 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 03:26:23 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 03:26:23 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce830fa77d4b115cfaf24b738e9446bf0a4f81376e032aa987524067c89ce862`  
		Last Modified: Tue, 04 Nov 2025 02:11:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7026c0eff48abd7d78b4d48e857190892698bd42ac1870678fd2b8de57810`  
		Last Modified: Tue, 04 Nov 2025 02:11:25 GMT  
		Size: 86.2 MB (86246181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fca13e30853296aa92fe2bd5cf478c9bd0345bb0626794c4f715f0fab50dacf`  
		Last Modified: Tue, 04 Nov 2025 02:11:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddafb09415aee4222be956d236bf88318a5c1f4e6d838965d4550891ead54ef5`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 3.8 MB (3752047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca5a42a71e4478c905cba648854cd77b37bbbc3f3984a4175f222d912b98ffb`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921b6d7488d1b9e60d0c102a94ac68a45f0c2c60f9e0a1e39a4c61bc5e1d2b47`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7da82159936cdb3c8e9fb4573f01e269214d291a13c84b089bd5c791b32e29`  
		Last Modified: Tue, 04 Nov 2025 02:14:29 GMT  
		Size: 12.8 MB (12755678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d86ec0fe955be1427b5f101652f0fa4664425c15ac79cf3bb8e40116c57d19`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b876f0bf06bc1d88e4be7413994208a5e4553b3437e4f0d004e86f6b08c7de`  
		Last Modified: Tue, 04 Nov 2025 02:14:29 GMT  
		Size: 10.1 MB (10066683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40ad92f467d2b4598352aa9814b1299007fedbd51844215eeddfecb007d016`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce92a2a50d9bc986ef6c8a19e28155d200597db1f617ed5e3f3fca7a38689e7`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3075b9da7dad44d6e9d89771a292dea20a3edc5ba6c7562ad8f9f0d4d892be`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc6a5eb14f0f55f865aad1d7dbe2ea9efe5b048ac4a61e37e0f8c56a4a5c328`  
		Last Modified: Tue, 04 Nov 2025 02:14:28 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0aae02ba28e6d95c1d301d2d5b5d60f1e04fa871aa7d60ab87ed026e99cb1`  
		Last Modified: Tue, 04 Nov 2025 03:26:45 GMT  
		Size: 19.7 MB (19724622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cc09d86745d20acec568fc25053ef0a4a3ac7e2b94cf4f1a60006908ff5d6`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 1.1 MB (1097890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f97d60ef6d5eb6bc8ae5325541022565e7ab538e871d998a0b060d42cc2ddd2`  
		Last Modified: Tue, 04 Nov 2025 03:26:47 GMT  
		Size: 44.8 MB (44798505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1977b83ad12c9e4db9d4846f104e790ff21137703651c36c0fd2644813237933`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d22f5e29a1d1a8a3643c8816b352b3af23197dc7a323dbf307148ae0b0d08`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c6bce5fd9c2140fc86629ad8d2f85f33c0398b8b07e19f00c2868f3bbdfd91`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0fc732a679ac69e12a8ea5247568f3c6c225835c06bf2eef298730added4a9`  
		Last Modified: Tue, 04 Nov 2025 03:26:43 GMT  
		Size: 18.4 MB (18394910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9d7588d3606d55bd0f59b55289163dba7408262762a1159ddce3af26ff647e`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9fb02408b16acd98214bdfb5457438fd0c452f0137d88de91c4b10ef41ffc0`  
		Last Modified: Tue, 04 Nov 2025 03:26:42 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:f25dc7e4f6bc6617d65a46de2349b9a803a76a9e630f87c6f145abb38722d04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c50cc3c9772920b982cd94dea877de33eb5bde72ec86b8d5cee859c4590c48`

```dockerfile
```

-	Layers:
	-	`sha256:e3974284a589d1e31e058d589a2337b1b4c4ea38df264bea5b0f17a4f176ad47`  
		Last Modified: Tue, 04 Nov 2025 12:29:16 GMT  
		Size: 65.9 KB (65944 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:eaf215069dad378809d438f5a3bb144b5937085b032174388af2f1f7a9e556c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257529922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0e3a289bae2ca51cb8028214c44b78b260bed839beca9e446e373ddcb3dddd`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 01:18:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 01:18:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:18:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 01:18:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 01:18:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 01:18:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 01:22:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 01:22:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 01:22:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 01:22:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 01:22:54 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 01:23:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 01:23:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:26:56 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:26:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:26:56 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:26:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:26:56 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 02:22:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 02:22:28 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 02:22:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:26:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:26:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 02:26:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 02:26:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 02:26:06 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 02:26:07 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 02:26:07 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 02:26:07 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 02:26:07 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 02:26:07 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 02:26:07 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 02:26:12 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 02:26:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 02:26:12 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 02:26:12 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 02:26:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2b692b585ba2e5d42e9ce2d0e15bf374b3cd47e5213a455ecd3adec6cfe2c`  
		Last Modified: Tue, 04 Nov 2025 01:22:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acb8871dca2fca7444c73b6887f851e400d8ec21ef90e24c32049edb92309b0`  
		Last Modified: Tue, 04 Nov 2025 01:22:59 GMT  
		Size: 110.2 MB (110162471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46535da4ca24054f9265e716c596399e6369dffd6050748b15f1e764947ac375`  
		Last Modified: Tue, 04 Nov 2025 01:22:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091e9758ec6b059c9779b24b92675750e477fff011f86c2c5ed8d697743edd08`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 4.3 MB (4302104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be29b22de8c1728227e75f1de1984dcae5a99ea150b8bf8beb4ced90dcdfb97`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b86ef0a1c48c8d88bf98b0fa38109cc6a43a7b9c4310a1d50f73cc75c678bb5`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a528684c2441dd0f58ff608b89750252f796b6c321b9a09e2ed35e55636356`  
		Last Modified: Tue, 04 Nov 2025 01:27:27 GMT  
		Size: 12.8 MB (12757562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f052a1d067a55882552ff3ce05a9255ef27f592b3f7501b6122d4548fb5fa3a`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb0c8fff0266a3179b7a2ff625136615ef3e4299228faa28a8dfa4f5187704b`  
		Last Modified: Tue, 04 Nov 2025 01:27:27 GMT  
		Size: 11.7 MB (11732828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818299ec9fdea088ae1378efd8dfb2c6bf30e5edbfd3109291a39c5dd35cf790`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b36d7f286479214fb47e08201a5227e6f7c635f7cb3fc406df87da08a70a2`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223290c4e4d459c8577e19049ec2a11ef5110d0c3291f886874da25247b90def`  
		Last Modified: Tue, 04 Nov 2025 01:27:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ff3e6a4c021eb7f9f1fc37b34bba517ab34e240dac43de6418b2041a22402f`  
		Last Modified: Tue, 04 Nov 2025 01:27:26 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01465445a479b98bdd0d3804b6afb293de7903e79f4ce7896d9ad18b8ee2c3e`  
		Last Modified: Tue, 04 Nov 2025 02:26:35 GMT  
		Size: 20.2 MB (20232472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec28bba31e23a7b8683d8a1d0776b511e85e2e9f5cb02203348b66b5e6314f5`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 1.1 MB (1064793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5f8efe39628233eef0e03c72fdaa86f92aa188b8d27e3f844fb1416c178422`  
		Last Modified: Tue, 04 Nov 2025 02:26:37 GMT  
		Size: 48.3 MB (48336804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6680721bd56d046ae231bd5a63299eacc56c3a59ca8ef78a87132f1a9e8d27c`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4bab8e2af6896e9f2955d3f05557b537342a96736e6ba7efca0ccf610dd348`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b927a0ee8182f8c1231b7af1734a7c54e0ab787b2e6143964ca2f5e8e2200`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19f1df7bd2709e337860971fde96eebe5fcb3408a02fddd3465018fcd1835a1`  
		Last Modified: Tue, 04 Nov 2025 02:26:35 GMT  
		Size: 18.8 MB (18786891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dfb1f5bf6c955f57040f7ac7728f9483b8437ababd0131f16336e2b5368cf6`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cb43fa2c273db2c8cf9a1456e1efa3cd3dc558409e7bf8d1f073f7a947b34f`  
		Last Modified: Tue, 04 Nov 2025 02:26:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:edbf8a067e5c0fb50070cde51b59d1c7dd8620504903617b8ea61793ebae7000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9053e04756cc2c07ee33eed22d994966fd01eb0a17991681598eabc0b45cac`

```dockerfile
```

-	Layers:
	-	`sha256:99a0649ab5a904d7478574e13114e1e9e5ff1f4ffdd4565ec70b63b36a7d3c37`  
		Last Modified: Tue, 04 Nov 2025 12:29:19 GMT  
		Size: 66.0 KB (65990 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; 386

```console
$ docker pull friendica@sha256:d6e4196a820fa8383b2d10b031e66f8fa39a520672c18b64ed94c4398be1300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267178107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143942f920026e36224c93c14c67ecd2cda50260477643544b43acd95e8a5679`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:20:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 01:20:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 01:20:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:20:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 01:20:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 01:20:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 01:20:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 01:24:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 01:24:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 01:24:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 01:24:49 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 01:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 01:24:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:27:53 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:27:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:27:53 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:27:53 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:27:53 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 02:21:55 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 02:22:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 02:22:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:25:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:25:13 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 02:25:13 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 02:25:13 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 02:25:13 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 02:25:13 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 02:25:13 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 02:25:13 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 02:25:13 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 02:25:13 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 02:25:13 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 02:25:19 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 02:25:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 02:25:19 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 02:25:19 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 02:25:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b6180f26bc5a5b8e9b2ea398be19ae76bc4b2d86cdd3bdd41f1b50e78ad75`  
		Last Modified: Tue, 04 Nov 2025 01:24:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869191ca8062e427c526390959a4027cdccd61738b8df13f1451ff3ba8e61289`  
		Last Modified: Tue, 04 Nov 2025 01:24:55 GMT  
		Size: 116.1 MB (116138462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727f709eb37a2d82b6d3bffb250e242a7028d0d718189459cdd85aae2b27edc8`  
		Last Modified: Tue, 04 Nov 2025 01:24:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6d54d62c5bd135bb674455845efb119059421be26f731dc6ec2631729a770`  
		Last Modified: Tue, 04 Nov 2025 01:28:12 GMT  
		Size: 4.5 MB (4455439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab5eeffef57b9682c7399743635e13912c76706f8f546943bf4f6ebd9e14363`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f677bb68f686d7e67d7307d520c96ef27c38116b7105b26adfa29fc7cc6b9`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efce88eb39332c8fb99ce15b9a663ad2414e87391fa766e32b653fad793d462`  
		Last Modified: Tue, 04 Nov 2025 01:28:17 GMT  
		Size: 12.8 MB (12756741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042af961bf704dc744d216a659291790f28909031cfea624d018f397f4367279`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66123af50ce48ff96c9e5fe70fa7b79019db52240bdf5e18c02d0ca2e26a33a`  
		Last Modified: Tue, 04 Nov 2025 01:28:13 GMT  
		Size: 11.9 MB (11918300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465644f372badf7d2d71540dbbc6724e3e7cda3c5003662dd716ffb2d8677222`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be082fe5c7bdb1d5335c07b50be8e4679512a1661e090747d01b1f9e87fe7f82`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148182320667c41f4ba74e96c13b473feb81721a37922ce26538dfc3456bc8f`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ed087359bdb16e0fcaa9dad0c3e96252342bced809a51d7a27a617784b5bd2`  
		Last Modified: Tue, 04 Nov 2025 01:28:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd09b7dc376efa7ab8efd2eca5963c111e1e4739380eafa0716d494bbe1fcef`  
		Last Modified: Tue, 04 Nov 2025 02:25:39 GMT  
		Size: 20.7 MB (20738288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f3853f8317a99a44db118a9e92ee8d388837de74c7bebb608c6127d91bffe6`  
		Last Modified: Tue, 04 Nov 2025 02:25:37 GMT  
		Size: 1.1 MB (1107415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0034777a1c7c857794eb17080922a998ef3982446c2272afcb0be3428c47ff`  
		Last Modified: Tue, 04 Nov 2025 02:25:43 GMT  
		Size: 49.5 MB (49451224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd98665f48b9fdbaeb939aa7ac24e80f819b38d2f9c412139432ba4155b87e`  
		Last Modified: Tue, 04 Nov 2025 02:25:36 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76f593f2d2a43bdacfc3ce2ed4524fc1435278bbd75cd9d27c8251838869649`  
		Last Modified: Tue, 04 Nov 2025 02:25:37 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6c92047ab4215d6b44fad3dc876d3485eed735546f87e91fcab88e121608ba`  
		Last Modified: Tue, 04 Nov 2025 02:25:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e793da4cb79b39cb25c33ff17bb9322c246a5befc260d5a005fe61eac7715b71`  
		Last Modified: Tue, 04 Nov 2025 02:25:38 GMT  
		Size: 19.3 MB (19305767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12e3f2891e4d9c8b6febd452507296861e067d9e8cff22fd25dd956a6e11c98`  
		Last Modified: Tue, 04 Nov 2025 02:25:37 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04057ae3270ecb1ebf74b931727f4e7a9557186937d90867e9b6abb42a7e5b97`  
		Last Modified: Tue, 04 Nov 2025 02:25:37 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:045d17c1af9bd7624070bb4eb3518a8c6479f334bf3e13ac757514937a896b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf5240632da7034d0c614999dc44cb75e18184e01838f83842bb49e8d48f33e`

```dockerfile
```

-	Layers:
	-	`sha256:211c0958274e1c06286687fc009793892db48947d458256be2d52e5de30172a7`  
		Last Modified: Tue, 04 Nov 2025 09:28:51 GMT  
		Size: 65.8 KB (65752 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; ppc64le

```console
$ docker pull friendica@sha256:6fdc7ee80f9bd88e61c74526a412380cfa695b74f07c17e2316d60305c4aa16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264536636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bdf49245110cfd5470a08a7f168098737e950a4a25ffb82a4a5310dde35951`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:13:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 02:13:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 02:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 02:19:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 02:19:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:19:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 02:19:27 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 03:44:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 03:44:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:48:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 03:48:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:48:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 03:48:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 03:48:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 03:48:01 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 03:48:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:48:02 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 03:48:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 03:48:02 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 17:14:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 17:15:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 17:15:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 17:20:17 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 17:20:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 17:20:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 17:20:17 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 17:20:18 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 17:20:18 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 17:20:18 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 17:20:18 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 17:20:18 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 17:20:18 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 17:20:18 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 17:20:31 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 17:20:32 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 17:20:32 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 17:20:32 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 17:20:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656e7846c7f44be5e3b20020683ff090edb2eb912594bbc202519629107b2cf`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b9ffc03561872af5426b43902b2fa8677357153c8026953c971daa576c870`  
		Last Modified: Tue, 04 Nov 2025 02:18:50 GMT  
		Size: 109.6 MB (109597848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf1f4cde3b0ec73324641d784753c77627b0db1a0e1c39f0478fd104a862fa`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a681e417318540a9f283d4aa7e32ce78499caf1d703a1d0d57eb1d0af73353`  
		Last Modified: Tue, 04 Nov 2025 02:24:28 GMT  
		Size: 4.9 MB (4875740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9f43a52bd1b3348a88fa49fa129ff29f21a40c48258c891f9cea413e78d5a`  
		Last Modified: Tue, 04 Nov 2025 02:24:26 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dd2964f9f59aa14ef577d3c0070dba5d511469bf96c546992cf281e3637962`  
		Last Modified: Tue, 04 Nov 2025 02:24:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fb182cb9045948cf3149e195d99f6b116519f6f850bdcf0ef8177d3b31bd55`  
		Last Modified: Tue, 04 Nov 2025 03:48:39 GMT  
		Size: 12.8 MB (12765942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321aa8133b08f286d9a87b764cdd1946763f3ed2b4050be19daa66b5a9282903`  
		Last Modified: Tue, 04 Nov 2025 03:48:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c091fc65e437136035a08479d07d164ab6a9fac12a64269ba8ed7838acf526eb`  
		Last Modified: Tue, 04 Nov 2025 03:48:39 GMT  
		Size: 12.1 MB (12118246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32495038ffabd31c0a11d661f33542e575979cb77780e73fb1ab997775ea38a4`  
		Last Modified: Tue, 04 Nov 2025 03:48:38 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fd362afaa998c2d1d5089903642a9c216ce92d3c60c56beeb8e04938f0da`  
		Last Modified: Tue, 04 Nov 2025 03:48:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c640637824b692743559aa94dcf3604e11142f7ea95f98e6dda13ae772c49a`  
		Last Modified: Tue, 04 Nov 2025 03:48:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b2844a2a88a0288653051efbdf999c4ae427b78aa216e44cd51873a129e89`  
		Last Modified: Tue, 04 Nov 2025 03:48:38 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139b74b4f8962d5f4b389ec3d1663140647b7a1935fff387f47091b1b7684f08`  
		Last Modified: Tue, 04 Nov 2025 17:21:05 GMT  
		Size: 20.7 MB (20686866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cfc61cfc9cde8fab791548eb765bd64fe3432679a36430006403c237faa10`  
		Last Modified: Tue, 04 Nov 2025 17:21:05 GMT  
		Size: 1.1 MB (1054940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92822a898b8ce4d70a4a054c8016cd2bebd43cef3a4dea2b9382da032a964343`  
		Last Modified: Tue, 04 Nov 2025 17:21:16 GMT  
		Size: 50.8 MB (50786742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7596357c2c15cf1086f9c859ec5f0e0a6d5d220e7423bc873ae7d29aba1cd2`  
		Last Modified: Tue, 04 Nov 2025 17:21:04 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0413219d0fe13364c879a3702b1b03f9b36ca31cb27c050ca9d749ec4cd5d7c`  
		Last Modified: Tue, 04 Nov 2025 17:21:04 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301624d495482dcd103ee3888e658a0d84ae6ae2e52bec3e4bcd42187a992882`  
		Last Modified: Tue, 04 Nov 2025 17:21:04 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb91c54d478302fc88ad287ab0063fe3664d6aa698231a079b4e580fa33eed`  
		Last Modified: Tue, 04 Nov 2025 17:21:06 GMT  
		Size: 19.0 MB (19039963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099f86e826342a231be34e86cf52db654539fe951a84c0f942f2a9d1164c57e`  
		Last Modified: Tue, 04 Nov 2025 17:21:04 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c62edbf0ce927093262f95f6aae4046872bbdb0a8c0ced77a015b4c04c4f87`  
		Last Modified: Tue, 04 Nov 2025 17:21:04 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:985f6806cd30d04cc287a68c5682e2ec090c7e702f2c5ebdec9b8479253bdedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5546e6372a0c9d5775d0f54e2398f5f7115b81a68a89de3fd327e0f0789eb95d`

```dockerfile
```

-	Layers:
	-	`sha256:15010f85c4b47fe84fefcf00b751c7afb758bf185b0f0b6646e610be506da21d`  
		Last Modified: Tue, 04 Nov 2025 18:28:46 GMT  
		Size: 65.9 KB (65852 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; riscv64

```console
$ docker pull friendica@sha256:9a0495b3e65066d65e8747cc3b8af88b566fc140e6eda35eaa441ce4f39d9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298690075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c17ff08db6c47e8048d4a40143d07a92ccb9433269fbbb190a999823f489324`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sun, 05 Oct 2025 11:30:48 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 05 Oct 2025 11:30:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 05 Oct 2025 11:30:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_VERSION=8.3.27
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 05 Oct 2025 11:30:48 GMT
STOPSIGNAL SIGWINCH
# Sun, 05 Oct 2025 11:30:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
WORKDIR /var/www/html
# Sun, 05 Oct 2025 11:30:48 GMT
EXPOSE map[80/tcp:{}]
# Sun, 05 Oct 2025 11:30:48 GMT
CMD ["apache2-foreground"]
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV GOSU_VERSION=1.17
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sun, 05 Oct 2025 11:30:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
VOLUME [/var/www/html]
# Sun, 05 Oct 2025 11:30:48 GMT
VOLUME [/var/www/data]
# Sun, 05 Oct 2025 11:30:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Sun, 05 Oct 2025 11:30:48 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Sun, 05 Oct 2025 11:30:48 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Sun, 05 Oct 2025 11:30:48 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
COPY *.sh upgrade.exclude / # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Sun, 05 Oct 2025 11:30:48 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sun, 05 Oct 2025 11:30:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e23c0c73cc8f0a9cca6c3668230538af936622d758ae4720124e65d1901fb`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a425a73dbb9980b18297b2dd5ae6470d5dd6bff4029928b3c47109bbcfc0163`  
		Last Modified: Tue, 21 Oct 2025 17:30:53 GMT  
		Size: 146.6 MB (146579498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0199b9324986716555eaee60a4139b64762a2ce7dc60435723ca0d60bbdcc8e7`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e411973bcee0512dfec874e20878187e9ca3d61e5e85f50bb8f0f0a7c12003b7`  
		Last Modified: Tue, 21 Oct 2025 07:00:42 GMT  
		Size: 4.0 MB (4026071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0db7f60aa00b9271b9f20a450a46ec36bd24e8cb67c827c82321a67378125a`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa6de92184bcc00f479d98e26a3d28b90d3c4dde823cbaff7b0da1c8aaa9a4d`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cb92dba7495529fba53b872099d496e924ce77806e49328869c593c68fcd56`  
		Last Modified: Sun, 26 Oct 2025 03:04:36 GMT  
		Size: 12.8 MB (12772470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e886069035ac2fe7026012b0bf9ed25301d912c3c93fc26d2d2686927644c`  
		Last Modified: Sun, 26 Oct 2025 03:04:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77138d1f73341de52cad7fbbba7ffe0fdbfcc641281ce0639ffd489301c7780b`  
		Last Modified: Sun, 26 Oct 2025 03:04:36 GMT  
		Size: 11.2 MB (11246684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb8860dad993aa1015e45a6f7ff67d658a0de128b8c5b3e4834b2335c7ea4ae`  
		Last Modified: Sun, 26 Oct 2025 03:04:34 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2bfca50a32f137ace9766c901338bffaf5f5716abf31d2e75849870aaa8db`  
		Last Modified: Sun, 26 Oct 2025 03:04:34 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5506f406a028d1accfdca3b791759d7fe8aa8ea818821cabb6ef2172e8e884e1`  
		Last Modified: Sun, 26 Oct 2025 03:04:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1061db126c27e2dc776cf9e306ba0b5316ba06c539ca2106293f87b9e06ee1`  
		Last Modified: Sun, 26 Oct 2025 03:04:35 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458f5ccca1624e111b71b91f3154c537cdc91c706a69e552eb1094667bb9c455`  
		Last Modified: Mon, 27 Oct 2025 07:20:20 GMT  
		Size: 19.9 MB (19891593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb6d1b1e05fd1df53b7fe36b0b786a40cb904a2bc2650d721ce9c21175490a8`  
		Last Modified: Mon, 27 Oct 2025 07:20:18 GMT  
		Size: 1.1 MB (1103280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144eee2a519dd088f8212aec70cb9108e656bca99018f50c8c30f1ef8e0e1cf9`  
		Last Modified: Mon, 27 Oct 2025 07:20:26 GMT  
		Size: 56.4 MB (56418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e168a014502965d62bb1060318b1cbbbeb97c685e88ac6dcfe4e7e64212af99`  
		Last Modified: Mon, 27 Oct 2025 07:20:18 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d19270970e53dd7609f700e3dc2b60a311ab6ef3dc92f7354e4f26e0febba6`  
		Last Modified: Mon, 27 Oct 2025 07:20:18 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2d590fd28ece98194cbabc9ab54034594e2c823051ad7de045f4fb825589b8`  
		Last Modified: Mon, 27 Oct 2025 07:20:18 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a595850632fabe530f27951eb48b771f42d9fa5a535a2a0dfdf9237fc5db05b`  
		Last Modified: Mon, 27 Oct 2025 07:20:24 GMT  
		Size: 18.4 MB (18364214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786a571b4e4c6a581d5888db07882adcf9cdbd8007108ea319af74eb021e2712`  
		Last Modified: Mon, 27 Oct 2025 07:20:18 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee6878197e2709113b100492d0b4fcbc95a6e8a6d281ea1d418941d82ad84f`  
		Last Modified: Mon, 27 Oct 2025 07:20:19 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:7afb72ae1d162d8b7ae897aba2f71615de768d5da0b6fb07c8d7d4999fe07706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967c08f81db1a09738b46a66855f83506ab9117ec90cb7c1efea774c7495fde`

```dockerfile
```

-	Layers:
	-	`sha256:e938d3cb44d4744f1e83296e540218b93ee6e7d253239ead04758b00a932f09c`  
		Last Modified: Mon, 27 Oct 2025 08:28:01 GMT  
		Size: 65.9 KB (65895 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; s390x

```console
$ docker pull friendica@sha256:4bdab473f39ebbdbef3921a48a2a5f929dd54ff40822f751b87c76f849a6c880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238482620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95f30db8f1bc752c7795ed830b98a3e6f2726507d3a2a556288e9c2a93d0f65`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:10:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 07:10:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 07:10:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:10:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 07:10:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 07:10:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 07:10:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 07:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 07:16:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 07:16:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 07:16:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 07:16:43 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 07:48:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 07:48:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 07:51:01 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 07:51:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:51:01 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 07:51:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 07:51:01 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 22:56:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 04 Nov 2025 22:56:28 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Nov 2025 22:56:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 22:58:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-7.q16-10-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 22:58:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Nov 2025 22:58:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Nov 2025 22:58:51 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 04 Nov 2025 22:58:51 GMT
RUN set -ex;     a2enmod headers rewrite remoteip;     {      echo RemoteIPHeader X-Forwarded-For;      echo RemoteIPTrustedProxy 127.0.0.0/8;      echo RemoteIPTrustedProxy 10.0.0.0/8;      echo RemoteIPTrustedProxy 172.16.0.0/12;      echo RemoteIPTrustedProxy 192.168.0.0/16;     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip; # buildkit
# Tue, 04 Nov 2025 22:58:52 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 04 Nov 2025 22:58:52 GMT
VOLUME [/var/www/html]
# Tue, 04 Nov 2025 22:58:52 GMT
VOLUME [/var/www/data]
# Tue, 04 Nov 2025 22:58:52 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 04 Nov 2025 22:58:52 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Tue, 04 Nov 2025 22:58:52 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Tue, 04 Nov 2025 22:58:56 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 04 Nov 2025 22:58:56 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 04 Nov 2025 22:58:56 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 04 Nov 2025 22:58:56 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 04 Nov 2025 22:58:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36ff40b0126c3c5915be8b245f7a0c59a01843dd27ab3ef36850fdb49c5f454`  
		Last Modified: Tue, 04 Nov 2025 07:16:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f593819f8b2a115d151973f19583dbea988a9eb30aaf3e8f29c91fb038ae3ac`  
		Last Modified: Tue, 04 Nov 2025 07:16:28 GMT  
		Size: 92.6 MB (92565502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd318b899472c8f49e2dec5b1b179e124a52f61ee0db5a8115b3592d8c71e59b`  
		Last Modified: Tue, 04 Nov 2025 07:16:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dfdd1fb72a08286c3d9449bcd6370f7722fc8b58bf4d0476de75f0374c72e6`  
		Last Modified: Tue, 04 Nov 2025 07:20:25 GMT  
		Size: 4.3 MB (4320533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df28106a2b22546e201757363f97606c7f310b763eb423a9bac19c613774221d`  
		Last Modified: Tue, 04 Nov 2025 07:20:25 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240566a6b10c21125e96873c058cce1547ec50832071b811a12ede3bda7bf283`  
		Last Modified: Tue, 04 Nov 2025 07:20:25 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39477ad367388daf8c40155f06507e637434996dea3e22d4355f15a501968f`  
		Last Modified: Tue, 04 Nov 2025 07:51:31 GMT  
		Size: 12.8 MB (12756437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b46e8fa8f4985458de46747a5a9bf76c2a8b3a17f1e73e4cbdbbc048b79c1f6`  
		Last Modified: Tue, 04 Nov 2025 07:51:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f1bae4845348cc3add8d790e5b70ee14972a6916737eedb0b6d1f29935a9b7`  
		Last Modified: Tue, 04 Nov 2025 07:51:31 GMT  
		Size: 11.6 MB (11565445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f992a511637a600783e8dce7482b62588a0f7919ce39ecd1d9a5e83c81bcc771`  
		Last Modified: Tue, 04 Nov 2025 07:51:29 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ff699b3b1dcabd68020959f5c6c31991bb996e7dad12a79b720c84e3a5be11`  
		Last Modified: Tue, 04 Nov 2025 07:51:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e208faf6da31d5fe8c7f4affe3818b671754b8a36f5d66979127426cb5f9c129`  
		Last Modified: Tue, 04 Nov 2025 07:51:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf5c696377b3f2b7cca5ca17aaf8d482f7de8cc335a8e703c17de8f850a30d9`  
		Last Modified: Tue, 04 Nov 2025 07:51:30 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b17006f3922a53006b9d4d94441ef587d8bdc963bff86413dedf257409dee9`  
		Last Modified: Tue, 04 Nov 2025 22:59:22 GMT  
		Size: 19.8 MB (19784749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa12dc9a254ebd4b17566ccdc730c873138c46e5122fbd918414f8359835137`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 1.1 MB (1097294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f5e873b2a59e1e035d198d51b8e0c72ee13f2fc1c690438dd2d9ffb1b2986`  
		Last Modified: Tue, 04 Nov 2025 22:59:30 GMT  
		Size: 48.2 MB (48216440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6bf377f95353dbef942a6fb6f29d7c9a38c92da0dabb440971ec907669c1b3`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6313172b5529a7b9def3d26a1dadc15d4a2aa1da9dda1a4bfab9d99712594e`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137d35374001ec287aeb91f607ee2b90661baa709128b475f14bdb276b7bca52`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334855863dcd6a55b0db9a9fb1c0a9c72d3c7f4d2398f362f6c30839a540020f`  
		Last Modified: Tue, 04 Nov 2025 22:59:22 GMT  
		Size: 18.3 MB (18327129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156bfbd4b30dea1f5045731e22ab892de58db8d44ba2692e649fb3f548dde36e`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c18e93e0b93a28ab24850632fe28da8660cd42bbb66f73d2e841bfc299e5706`  
		Last Modified: Tue, 04 Nov 2025 22:59:20 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:e54750ace9d556920f4a5640556382dc669ae2bb7ce56b9b25c732bf546b8215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6cc2b9fdc404db06cf47777b1d1d6635c1dbf3656039702465e661f26d442a`

```dockerfile
```

-	Layers:
	-	`sha256:ca1220351d68d5e0fb4bcbdf91043591e2a9f6ce82a21d1f9383dc0188e5d87e`  
		Last Modified: Wed, 05 Nov 2025 00:28:03 GMT  
		Size: 65.8 KB (65786 bytes)  
		MIME: application/vnd.in-toto+json
