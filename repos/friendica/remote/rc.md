## `friendica:rc`

```console
$ docker pull friendica@sha256:7ed67b02fcb0bb7991c984b4552e9eaba38758864201732b8d541c17b7ac031f
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
$ docker pull friendica@sha256:bb060b71635db46c6f75e8fc97b580675e11f43932f24d8297e84ce6be8b6ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265981927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6047dce91f3a12fcf9ae6f23dc5cd22670cf0f29d6bd71ecbf611667afbaaf8e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e92096cc35bc9b7e1376cbbe9e6dd7abc1b5434263195038932e70d641aac`  
		Last Modified: Fri, 26 Sep 2025 22:11:15 GMT  
		Size: 20.5 MB (20455546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10071263777ef86f8e42c5bbc171ffa7f2bc2a871f79ee63ef705131169c33cd`  
		Last Modified: Fri, 26 Sep 2025 22:11:13 GMT  
		Size: 1.1 MB (1132823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d296390234c4a86b1b6f160f35fec4f9c3e6316ec55c0c7533495a0051cb6a76`  
		Last Modified: Fri, 26 Sep 2025 22:11:17 GMT  
		Size: 49.2 MB (49201555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ef3c9b7f9e00c2be146e54741893e2d632b36f7d8a80431eefe82bed8e1d81`  
		Last Modified: Fri, 26 Sep 2025 22:11:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ea24216796643cee8485c8193275f617c556816d45dc12a052a1c0df178912`  
		Last Modified: Fri, 26 Sep 2025 22:11:13 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeca7a482c43e5e9b2475c25c4350529e5dbb97b1ff98d36f10f9deedb1bf45d`  
		Last Modified: Fri, 26 Sep 2025 22:11:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba680a508f6b16da9c99d862a839b5c985b569ad40da44cd001d777fc61b724`  
		Last Modified: Fri, 26 Sep 2025 22:11:15 GMT  
		Size: 18.9 MB (18888793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00190d0e872bc295a74172fd545dab076aae2e010cb208436e3d6ffdc8c1eb`  
		Last Modified: Fri, 26 Sep 2025 22:11:13 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3605f0cdafd1553cfcb18b0a9fa3756632c470139d8d2f49a4d2ff40508adb7e`  
		Last Modified: Fri, 26 Sep 2025 22:11:14 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:4265edff839d42fe9b727c7d580bb1c79d0063b2845129c107d79a4923ae4e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caddaca514295e62b8a77b3d90d5434d023bc88e855f0e2c4d530ef932b73bf1`

```dockerfile
```

-	Layers:
	-	`sha256:b951c2afe77a32d676847fff4ffa252a4c7efd83b9ad1688ad5574fc30c4e5e1`  
		Last Modified: Fri, 26 Sep 2025 23:30:45 GMT  
		Size: 65.8 KB (65839 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm variant v5

```console
$ docker pull friendica@sha256:2c4449d84aab5e15ab76467e3ca05a62055a247efd212db2d62b2297fa7bf565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236087678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d405c3047f7b1bb58e93ac18d3f55062085f759946d023bc4822263157b1e6e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76066041e0b9450512a23fb0419b9b2682efa515fdb4324918ce63b20693991`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b577bb618d3e8ed2f9ac9c91a47f2ed4aa067f80e36b5bcdd0af6eb4f8a43788`  
		Last Modified: Fri, 26 Sep 2025 21:58:25 GMT  
		Size: 94.9 MB (94873927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161d21d49b3966740cf8c94b6cffe0e33bedce00a90cd9cca58beabd72de76f`  
		Last Modified: Fri, 26 Sep 2025 21:58:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0354b62f8b0f833a4f4db815a0b06971b870e72567f3dcb1148aaf3eda5f80f6`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 4.1 MB (4082002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891068cbea8aa706e605c4634e7f17e339e42e11bff5fb688b2ac9f755b80fb3`  
		Last Modified: Fri, 26 Sep 2025 21:58:19 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb4e28ff315032d3eaafb538ac9663dd911f2ffe3afd2e914d79262c0796bd5`  
		Last Modified: Fri, 26 Sep 2025 21:58:19 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0494101bccc0d3acf00b4ce7f606acb158e28c1facd4fa090f27457bc84cd03`  
		Last Modified: Fri, 26 Sep 2025 21:58:21 GMT  
		Size: 12.7 MB (12744125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b601f9f45852be9ba113b028882d148a0411d82d68cb41a57c9b7371c7304d`  
		Last Modified: Fri, 26 Sep 2025 21:58:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0f2fdc02e3294eab42ecfe45033cebe20ed9bb7e36a2859fe0d821b45b8c8f`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 10.6 MB (10591544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9bfad8500c874d442b750273a094284d02676de5c5c8fcc164481a81138b9e`  
		Last Modified: Fri, 26 Sep 2025 21:58:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c0b7a319b9873417b38ddeb9d12dfde0b4e0ccb5b21e9d1c177d341b2042f7`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d563de39040749a9547f938abaaf2e5a998a35b62aaacf477a7d9f20d6382`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8416a597755e2699eaabc24f41c7c26ee6ddbf12f00b4644783884cd3c8b631`  
		Last Modified: Fri, 26 Sep 2025 21:58:20 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27ba6dee0706abee8a31914334d05a0f25faa690823c834576df25485e6688a`  
		Last Modified: Fri, 26 Sep 2025 22:22:59 GMT  
		Size: 19.8 MB (19796463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc2c760d15056f5727a27e8c35aa3288a6e90fa4ca75b7ec7220d15d7b2af1`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 1.1 MB (1107519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33ac08e3a09eb4c970a5d17015473e4d785c93a240986f40803afdf8145e14a`  
		Last Modified: Fri, 26 Sep 2025 22:23:00 GMT  
		Size: 46.5 MB (46537119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccc667b607b303f0c0cbd7cdafc8f2bd1eeefb20c505b6b576f66fb6b612f21`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7f885f255cabee90fa41520652c6cc4aa72f51c18dd3f2bb753eae60372be`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567185a059965f9ec49acf3defe948ba493c9ad99ee1947fefe634d53ee959c4`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c6579ad61559dcf6dfbc34d8fd182d71392dd92cb992996cea5d2a65573a6`  
		Last Modified: Fri, 26 Sep 2025 22:22:59 GMT  
		Size: 18.4 MB (18401384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce107dcefc35c1caa9d705039b3e0cfbfbceca25832bbce8e11da16784e8dd55`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1974af24b71087ca67f02e2dc99e23abc03a0413525819ae5d592389984ba7`  
		Last Modified: Fri, 26 Sep 2025 22:22:57 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:1fe82405be49dfb82c629b0ce16b53429d656018f29c211d11925cae0375c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb57b689e564bb846c94e5cd629a87a60c47b93b69402bc4b5f1d6c650098997`

```dockerfile
```

-	Layers:
	-	`sha256:bbfff104dd4634b29229c1056641dde5fb893100d49cd614bd92e52ddf8dd201`  
		Last Modified: Fri, 26 Sep 2025 23:30:48 GMT  
		Size: 66.0 KB (65987 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm variant v7

```console
$ docker pull friendica@sha256:ba773c96b3c27090a5900571645fa19616486868d60d8cd14300a51af05fea83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222957972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7328128185f42aac9eb5fdd6b705f076c375ef1e14505af89938429aec4f1893`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7d5cf7252c753225b97f727ce038e74b0a7440e57bb6b6f0793e1418532f58`  
		Last Modified: Fri, 26 Sep 2025 21:40:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05c411730cbb5b10f410db21b24f488ccf9dc0624b859afcf14256060d57b0`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 86.2 MB (86245147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0375b5e06e5d699733d94254b5b9873bf52a9d9b8857b37f0e9dd5e2bd727e`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95d0c59915be11ae6b7ba4e8b25775f6210e57bba40406616f9db067f85e3f9`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 3.8 MB (3751919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b41bcf9bcc7e8c9c04a7d31c71313e984a6336ba43c8996b7d316fcd7227794`  
		Last Modified: Fri, 26 Sep 2025 21:40:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0019601332b94c0ad34c2b4b0d47731ede1bf963f4b2bf801a1f998627d3bc15`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f91febe5bdd14bf8191daf2323c2c9cf23d6e1dc0e9297c4317b3288f6e51fd`  
		Last Modified: Fri, 26 Sep 2025 21:50:27 GMT  
		Size: 12.7 MB (12744261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a3998bea4a28cdb11fd5372cd59136d5a5c45bf74e9f0a236d3676faf18d83`  
		Last Modified: Fri, 26 Sep 2025 21:50:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aed6b2c15f8a6c0a180a5122809615e94ee1b435ad41fd1ac42b4b83f204daf`  
		Last Modified: Fri, 26 Sep 2025 21:50:27 GMT  
		Size: 10.1 MB (10064269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72addbc7067a5bcaf10061dd405f0f06cdbf9fb0c91ec4884eacabc108c2954d`  
		Last Modified: Fri, 26 Sep 2025 21:50:26 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347804aa9a3a1e509f0d3d92074a933bd517778c62170229bb66dcc13cac9119`  
		Last Modified: Fri, 26 Sep 2025 21:50:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb065d51f9001dc5b669bffd7b82cc8905e41178eab957f31898e786a1bb4b84`  
		Last Modified: Fri, 26 Sep 2025 21:50:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abd6b84ce8b387eb413b22a20f85409859b884bb476f6509e47eb1958ff36e7`  
		Last Modified: Fri, 26 Sep 2025 21:50:27 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478ad77bd6596de25e4799a6116d871441f144d0f0adde22209f901ea4769677`  
		Last Modified: Fri, 26 Sep 2025 22:11:19 GMT  
		Size: 19.7 MB (19678367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a21b41d1cc247dc981be35b060c96e15e62bb3fba29f1eff2a44b912eda97e`  
		Last Modified: Fri, 26 Sep 2025 22:11:18 GMT  
		Size: 1.1 MB (1097910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a2eb95b427ec4f6637712b9f05edbe0eef12ce492afb89fbd2c639404748d3`  
		Last Modified: Fri, 26 Sep 2025 22:11:38 GMT  
		Size: 44.8 MB (44798458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ac36a0c006c2e63318acdf9f2cd2ad9f6e74e464c3a43cfa4a8fdb787143e`  
		Last Modified: Fri, 26 Sep 2025 22:11:18 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bd83bd4c04606ec90ead14057a3b00bef24f3b62a25e738f20bad33a89ced8`  
		Last Modified: Fri, 26 Sep 2025 22:11:19 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccf15eb0d9a511292f4fc0f69f732b15fcbdcb4ae72deb965855f4b8fe76547`  
		Last Modified: Fri, 26 Sep 2025 22:11:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3695c95195f63c6e362b256749b3168ed667f552b3f2c9698729712cfdfcba1f`  
		Last Modified: Fri, 26 Sep 2025 22:11:21 GMT  
		Size: 18.4 MB (18357969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2519e38016472b596a2e8ba9dd560db6f56a8577ee6fb44158b51ed602b26ee2`  
		Last Modified: Fri, 26 Sep 2025 22:11:20 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea422a43e107fbf70a3a7ac109a207b11c1d2d0b6d5a7cfb2a5d4feb368177a7`  
		Last Modified: Fri, 26 Sep 2025 22:11:20 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:a2ce388702dab14d4fe6916dac3146fcca51c2b2f830f0d0546c10379a166b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478800178eaebfc6b0c7341a0b51c72aec5368932035b516487c7128ba36c309`

```dockerfile
```

-	Layers:
	-	`sha256:5d3cc7a9ef04ab71b4c91aa79c009c375c6b4dd9f4809f7b0f69c47e8ed2554b`  
		Last Modified: Fri, 26 Sep 2025 23:30:51 GMT  
		Size: 66.0 KB (65987 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:fbfde86c73c02a81a0efe41d1a4af81977285787289892379d9a6ee80192082f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257442908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000d0dad64c70a4133ce490fbe1a5d4163580fd806d3bbaef142cab53566777c`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd3be9e19d47013e362c5a543124e348a78e45c7825f77010354b0469e97af9`  
		Last Modified: Fri, 26 Sep 2025 22:10:08 GMT  
		Size: 20.2 MB (20196254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4a2c6e18bd5e1bc7e45f3d2f532107dfddeed220cd960ed20d74806d489a8e`  
		Last Modified: Fri, 26 Sep 2025 22:10:08 GMT  
		Size: 1.1 MB (1064800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89100a41560aed64adcead36a4ba850e3b6f640c248b0382446615de33bc33e3`  
		Last Modified: Fri, 26 Sep 2025 22:10:11 GMT  
		Size: 48.3 MB (48336371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a95d64720b5f1c0b9192c1f26fffdc2a51d20707612fb0a859743f63c6aee79`  
		Last Modified: Fri, 26 Sep 2025 22:10:07 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b887356a7cd9d97fd7196c54c45a42084989d8fba0dc929a057041d2e1077c`  
		Last Modified: Fri, 26 Sep 2025 22:10:07 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b17b3c66432e391b8d57103704e25f04e81af9b0ab8421d5a74a3cd9e2a07d`  
		Last Modified: Fri, 26 Sep 2025 22:10:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28c728b79a6f24a071c64004f4abeba4da9a614008f275a12d1537be8e1427e`  
		Last Modified: Fri, 26 Sep 2025 22:10:10 GMT  
		Size: 18.8 MB (18753887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859d14f35c0118f91daabc0c7e661a3fdc82cd15474552ad37bc57fce88aa72`  
		Last Modified: Fri, 26 Sep 2025 22:10:07 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2273e7ac2c8b74c75fbc41782dd3697b7b6c489e84007a4a38593320d772e2d4`  
		Last Modified: Fri, 26 Sep 2025 22:10:07 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:99148789dd21558557d611028098518846bfefa2b557c2f056a2c13dd6576b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (66033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4591bc5f1fb605f9701d31a1bdfbe8f6002eb2e20df0c9b2c78f5480bc42f84`

```dockerfile
```

-	Layers:
	-	`sha256:d73b043bbe1cd1ca019cc79686f53ff9caee6bffe6179c3d84a31e57b1f97af0`  
		Last Modified: Fri, 26 Sep 2025 23:30:54 GMT  
		Size: 66.0 KB (66033 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; 386

```console
$ docker pull friendica@sha256:178e53fb207819b14221c8a8e575c2a61024b048111657f26928e1038f22d8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267083355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d8753bf5f8c04f0f30ba043c6f30b16998ff831a576986653aa53d65c2ebfa`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5e7d2873ac957ef8cc59bcd6e31b535bd2801ea28a57e1501fdb8e58608c0`  
		Last Modified: Fri, 26 Sep 2025 21:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef98b4ce4f1308179852340296ad4e0842b187b308af2b9ba1fd3dde24e81147`  
		Last Modified: Fri, 26 Sep 2025 21:41:22 GMT  
		Size: 116.1 MB (116138311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8036dbcba317aea50d2562771c8c84fe10a0034cc449b265008b58f4ece50351`  
		Last Modified: Fri, 26 Sep 2025 21:41:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b17d4530b858844de2746f5ae39e48378580106a23c18d6a049c1c007486dd2`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 4.5 MB (4455427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af9419965f19af6a0ed146dcddb7051dc1ae37ee589060f3704447734b7b89c`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a180c14a449ab6f79b7bb2b016f89e348f21388174ca1518cff540480ecc79d`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b8e5b9c4a4037ce010900cdcd44203506d462ad497a2e0cee8a3762d8c23ea`  
		Last Modified: Fri, 26 Sep 2025 21:48:40 GMT  
		Size: 12.7 MB (12745636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb444d0882145e4279a1316df6868621b74d48884fb06558b747a5a71c73e55`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323e83bee7d5a3dd2cca743477de43b9349e339e5f537e3ba40de6fcf37fc924`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 11.9 MB (11917028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec9a96d0306cabef7379523e9e3f293e8c9c224c38d9c3ca3e95436f0b60af7`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef923f37adc06493abc58e3efd9c1b89a52b83f5b83a3469f14f04e9d64b721`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbe3766524fe69b6c994c665010974e6c72dd83e76f29fc53bcf818e89cd51c`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee11cce12554cda8406355b75d1c54964f2fa1b109bcc7715777b2eb9ab9f90`  
		Last Modified: Fri, 26 Sep 2025 21:48:39 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85c8f1b35717b97d418138e5584639f050aa0fbbbf5bbe7f8634558a55b566`  
		Last Modified: Fri, 26 Sep 2025 22:12:59 GMT  
		Size: 20.7 MB (20701355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841c23eb4ed826499c1f0b90034a14eb83e13b7002595dfccb1b704a795457d`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 1.1 MB (1107424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1f81bec55eb73d272e13f0e29704be94fa5814868dc4705bea8c49e4fb8d2d`  
		Last Modified: Fri, 26 Sep 2025 22:13:02 GMT  
		Size: 49.5 MB (49450869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd25d5cf1ab0543c5401d1404e3f98abd907461c786d5281371d1eb741f50835`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c7c298bd7737afb61484c4dd9c3570dc47edc9ab15e32eb4c25142df6dd5b0`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e646538fdabc1c22f4447199babcc04ba7a6689de7c490d875e346d053572`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abbb6017f7ce3e80a820b4d1804cabdb072c19ac6cb1b9106457ab2026aede2`  
		Last Modified: Fri, 26 Sep 2025 22:12:57 GMT  
		Size: 19.3 MB (19265681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02dd995e506222ddac25940204e774579bcb7f572cbbe1fc78a6b84fc077983`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e627bd21865e3743660636002a2e66e34e00cb1e31ccd6d9c6c4357b65c7e9`  
		Last Modified: Fri, 26 Sep 2025 22:12:56 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:1d3a1d89c62df53d87d0019728f064ff8deafdc8e82601a5f6f4f8d1f6414c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bb4205bd47c68c01fefe6031a4638058df1239d7447479af6f5f6e1a837c5`

```dockerfile
```

-	Layers:
	-	`sha256:49d7e873ae5227221984a3d47a44f636e79c9a330eb500a333fc1822440606c3`  
		Last Modified: Fri, 26 Sep 2025 23:30:57 GMT  
		Size: 65.8 KB (65794 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; ppc64le

```console
$ docker pull friendica@sha256:347a65c2609841814cc86d9ac603f42b71efe65992c415564400975a9bf9a805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264431939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b779fd6fab5dca47509898d2eea76553802642161e03a49ce36c97fd5b73a3`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb5a7c2ec964eef33815fc315209dc7259500f176c00afeea12dce7c2622677`  
		Last Modified: Mon, 08 Sep 2025 23:13:09 GMT  
		Size: 4.9 MB (4875556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133daf04d0a4d1719a190dde5b767dcf5cb67060f9891ee35f0f786a618e0699`  
		Last Modified: Mon, 08 Sep 2025 22:47:21 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8262f8dc896e13cd1eb8cc0b98965b00768f23f0b8b2ca4eb70fd73e0c4d3`  
		Last Modified: Mon, 08 Sep 2025 22:47:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8a59762f7e64d08267345241119cce6d74e07715cc693ea8de0782b21ff86`  
		Last Modified: Fri, 26 Sep 2025 22:44:13 GMT  
		Size: 12.8 MB (12760722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44be8c63fdef3416aa2dc08dc254ea89d1daafe5fde356b3aa7c6c88838d4772`  
		Last Modified: Fri, 26 Sep 2025 22:44:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6ec05fce8154b48c64aa56fa1091321033b254ef91e8a79f4771f4673a2d32`  
		Last Modified: Fri, 26 Sep 2025 22:44:13 GMT  
		Size: 12.1 MB (12116923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fad8e8849302c1e04ad7a90cc3e388a829e68d76bc021a8684b2b2d167f918`  
		Last Modified: Fri, 26 Sep 2025 22:44:12 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fb890552173b8b5f41ae91f1ef768ebed4697b0ab6856e02b9cb0db9b53756`  
		Last Modified: Fri, 26 Sep 2025 22:44:12 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfb717c59e63d834a61226796a5bf6f443c42e719c9d23035c9dd86ee318632`  
		Last Modified: Fri, 26 Sep 2025 22:44:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b22e4a04f7161aea0dbf402cdd2249b5458e329beaaac23f4d7c281936c76e`  
		Last Modified: Fri, 26 Sep 2025 22:44:12 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b4194143c18f862b9ced6385014b08e859c6ac19eab28fd0053a15a8b72ac`  
		Last Modified: Sat, 27 Sep 2025 02:29:23 GMT  
		Size: 20.6 MB (20633408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709fe0c9eaaf7dd5e0a7d44937b08bb15c95af92d4bc58525dc83c3c61f7472c`  
		Last Modified: Sat, 27 Sep 2025 01:08:42 GMT  
		Size: 1.1 MB (1054750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c0b3077e4189b90de45af486b4bfdb752b72eb59b04bad1529dd1e45954e84`  
		Last Modified: Sat, 27 Sep 2025 02:29:24 GMT  
		Size: 50.8 MB (50785616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6735c719e3dafc0c82703c85bd262495e0b2a952c0ec7907957d4cf3249d6fb9`  
		Last Modified: Sat, 27 Sep 2025 01:08:42 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3059b430da41643a332f20f6c7d62d898f62084839f95c8e0db183bc97ced8`  
		Last Modified: Sat, 27 Sep 2025 01:08:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb660ad5ea6cefd32aa903d06c39293ec59db9031b041db561e9ce9edccae74`  
		Last Modified: Sat, 27 Sep 2025 01:08:41 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e3e3138e4e176f46276649cfe5e90882fb23e893a24835b84a47cee12d1e5`  
		Last Modified: Sat, 27 Sep 2025 02:29:22 GMT  
		Size: 19.0 MB (19002096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9f6fbb6ccf6979dc9b8eceef0e9a1402968d7532cff673a9c8ae0d6ffb8d7a`  
		Last Modified: Sat, 27 Sep 2025 01:08:41 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3220d3b6b7b57f060af3ee430cff0a3ec34b5593cf524ec156d83ccb045b5cde`  
		Last Modified: Sat, 27 Sep 2025 01:08:41 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:39a13f66ebcd27491bdea50f3b4b149c5b36a3418b7d76db8c0b28ecdcd3fab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955bd607207c7867080bca436f5311e0ef01cab2003702e88821783579e3ecd7`

```dockerfile
```

-	Layers:
	-	`sha256:371c0327cd43018ad9273cc2738173e427ed4d4c5dd2591457d632376965d33a`  
		Last Modified: Sat, 27 Sep 2025 02:29:05 GMT  
		Size: 65.9 KB (65895 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; riscv64

```console
$ docker pull friendica@sha256:eeb24e419e0203bac03d835f4b767188dad4b40de539fd8e14eab641ae4dfa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298598244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94931ae98c37d8a4c9bdd3924e450dc80c5b65ce9ea92d4c6e818d4198313a4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 28 Aug 2025 15:22:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Aug 2025 15:22:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae3e77da310b8f6abd1c47c2c908b688364ff453788dffc1ea3755bda9a618`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25a2ea3673eda57f8891f3fdc7a2b5bd7baa28ce076ff3427218ba02258d5f`  
		Last Modified: Tue, 09 Sep 2025 20:58:30 GMT  
		Size: 146.6 MB (146579169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd9eb164bef808ab9cc8b8afd7d2a60572baa81f3ff4c56c34d90a36945fb1`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1d685c22b2a71e0ac90af447b986ccd452c8bf3b3279addf81fabe668d6190`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 4.0 MB (4026102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3b33f48477a8d3d6159781343071903515e9a5e4e3a498f12132dc4e16087`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31a861095607a227987a9645651b2b7a18d0f30647655179a2cb5c863f10929`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92061bdf27713bdadbe8397100e169bb753f073a7a4ef8f3f7d856b8f7ec8e6`  
		Last Modified: Wed, 10 Sep 2025 03:56:32 GMT  
		Size: 12.8 MB (12756345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898c08a515fd6771e45fdc4888e5e7aced5bba3285d4c7365fa7155a0d24bbb6`  
		Last Modified: Wed, 10 Sep 2025 03:56:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9026b8a6eb7f16b1d4faebed07e7a22d1938a3f50efcb45b5707340eb7b12`  
		Last Modified: Wed, 10 Sep 2025 03:56:32 GMT  
		Size: 11.2 MB (11249238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc30c5331990479c3e942a274a7e047c7046073c84bd0b31d1e48c531add20b`  
		Last Modified: Wed, 10 Sep 2025 03:56:31 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb50eb33a47ef68824d1fc91051ff2aa59db1a9fa9182055c9a602ac8c54e0`  
		Last Modified: Wed, 10 Sep 2025 03:56:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8c3864f627ad73099e19e8482219a6773bdf15a53b0c491be8dc151ca50556`  
		Last Modified: Wed, 10 Sep 2025 03:56:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d30ad0855b5a2c9ad197b1a182c678da1bd3b5446c0d7e5d9ccf8849a7584f`  
		Last Modified: Wed, 10 Sep 2025 03:56:31 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4457e9af1943043d682f6b4b02e9264c4137ac48bd89031e0bfaf6d071b28ba7`  
		Last Modified: Fri, 12 Sep 2025 04:56:26 GMT  
		Size: 19.9 MB (19855289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6eda8def16991a670149154619dc759248a484c8c6d5f28ee7d24fa463485`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 1.1 MB (1103294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201bcd2471c7033707550dad5729696e443e7a5f7817b87bbd773aefe3624f2`  
		Last Modified: Fri, 12 Sep 2025 04:56:46 GMT  
		Size: 56.4 MB (56418811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff4292a3eaa4ef71bff9623a21ea488e1941289cf0e2ef76f6bbd5c84c3f5ad`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318be3875439b80840f08d5686308ba2ab5d289b2851fe3aa0d69ce85ee80a7`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34b6998e50f8a810a01784fee12994c8ab464ef94e9aa8a465893990b752c88`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2385c6c983d2ff26b6ce05dac97bf02f78ee1fe412687d97616bcf5a48ffd1`  
		Last Modified: Fri, 12 Sep 2025 04:56:29 GMT  
		Size: 18.3 MB (18326750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd4d8402be5f3e12ee1ae0cf2d278f3569cc8f099bf80e98505d3ead3c6d23`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9fcd215257b6f9ddc4ba285a8497e76a19119bc193a680bd47aba49011050f`  
		Last Modified: Fri, 12 Sep 2025 04:56:22 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:495f35b0ef8bfcddc2ffe014cb9ea88a6e79628eb70ffd21b07a1a68e7049ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b83317892d42c8da457412cf0fd94c3dad010d31f535f3fcc08ae4e1a4b4d8`

```dockerfile
```

-	Layers:
	-	`sha256:9df2fd2eeb007e9d7a636064e3d0b89e5e0b311e11aed805ea5505a30ef796ff`  
		Last Modified: Fri, 12 Sep 2025 05:27:49 GMT  
		Size: 65.9 KB (65895 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc` - linux; s390x

```console
$ docker pull friendica@sha256:02d4cd53e627119f37455af620e4146bb9c907a6569195cbf83b28636e390700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238387767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e1da81bba08a0a484b8711bf0a6fd8e5da89c92f348c01d4dc3f66c598df7b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 30 Aug 2025 22:12:39 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f633efb1bb21ecc579e196bca25f5ab7d52d7c2db3ee2a067ee60f0f9c012`  
		Last Modified: Tue, 09 Sep 2025 00:03:06 GMT  
		Size: 4.3 MB (4320437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c2cf9f6a014fa655f3eb4189a487c63fa210b55a95d802554be23b3bcfe1cf`  
		Last Modified: Mon, 08 Sep 2025 21:55:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bab93bff6df540c8c28fd0c65b5629bb7a3784cb5470795e60ecbef3aa18f1`  
		Last Modified: Mon, 08 Sep 2025 21:55:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707051d1a9c01608f6de1a0ae7a96c9407b5ae6a13cc5af8fd85c8b99a638c24`  
		Last Modified: Sat, 27 Sep 2025 00:14:58 GMT  
		Size: 12.8 MB (12759962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84569c80ddd5b7702f86d68d7d735256270e56a012ac0e738302d50776bc651`  
		Last Modified: Sat, 27 Sep 2025 00:14:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1504318b3a54219adf0ebb26ed294a096d8cac08c005d83a9e3e46a09c1784b`  
		Last Modified: Sat, 27 Sep 2025 00:14:58 GMT  
		Size: 11.6 MB (11562553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aee97a07ce4f23b7e6904400a418fcdd968760d6c6881bae04579102a4df6c`  
		Last Modified: Sat, 27 Sep 2025 00:14:57 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c754fe975fa8af566f87d9efc38ea7b51428f7210b315bb7319fc6ca8a9a3d8a`  
		Last Modified: Sat, 27 Sep 2025 00:14:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b788284e1a0c850b05571c9d0be2db8dde65d1ac16085dd65e3821fa69b7d3b`  
		Last Modified: Sat, 27 Sep 2025 00:14:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e9ae3b4466bfa3be02d3a5457243ca8357b93f77df5b666668a4cfbddbb83`  
		Last Modified: Sat, 27 Sep 2025 00:14:57 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d72d2d91a3d8af04a1cf0ae43fcfef6aaa85a5d47329f8cefd96b68bc4fa39`  
		Last Modified: Sat, 27 Sep 2025 02:16:29 GMT  
		Size: 19.7 MB (19734191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bb9cbf9e9fc888c10b3948dc939a91061febe552d0c828b6b7aa1ad9ab70b1`  
		Last Modified: Sat, 27 Sep 2025 02:16:29 GMT  
		Size: 1.1 MB (1097224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8d5e28fb604540e6a99f50fe7ef520eb6428348a6b607c8538ab7cefe92006`  
		Last Modified: Sat, 27 Sep 2025 02:16:31 GMT  
		Size: 48.2 MB (48216290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b0c6d5a2be28df33278dc04307c5a3d0ed8daf27f0a0ca2afb5da7005f7ee`  
		Last Modified: Sat, 27 Sep 2025 02:16:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa81ec50779261a5e8177ae60c65f12eb92dbba52b5724063046d93cd70ffaa`  
		Last Modified: Sat, 27 Sep 2025 02:16:28 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d336af69bdef6bee4684829c120db3493fa36bb2ef1f4a548343f59ece0f3b`  
		Last Modified: Sat, 27 Sep 2025 02:16:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95bdb842b854f35ffee59dc914b597441e2eaf63f91d8438a64b4b7fb49dc3a`  
		Last Modified: Sat, 27 Sep 2025 02:16:29 GMT  
		Size: 18.3 MB (18289844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ea616e18c800a2c6fae6529983620c321f613e9e36ef5b512738e93af55bea`  
		Last Modified: Sat, 27 Sep 2025 02:16:28 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b5294fdcdd0bdda32d3f5ae09fc85a7d4c91329e19ac3023311eb13c7d28c1`  
		Last Modified: Sat, 27 Sep 2025 02:16:28 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc` - unknown; unknown

```console
$ docker pull friendica@sha256:107a64de1314aada3ad4ba98de4882bc7bf3455f6518b319d5bb896899bf3f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da69c2d125aaae0f0762f0922d1e5a04481b265b7663089cda72205a04e01c92`

```dockerfile
```

-	Layers:
	-	`sha256:3b0464e113a9dcdc14f7acaaf20cba04034c2414a060b87cb6fe94767d803e46`  
		Last Modified: Sat, 27 Sep 2025 05:27:59 GMT  
		Size: 65.8 KB (65829 bytes)  
		MIME: application/vnd.in-toto+json
