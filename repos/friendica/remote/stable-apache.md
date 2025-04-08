## `friendica:stable-apache`

```console
$ docker pull friendica@sha256:a2c3cc2adb1b17cfce6eceb954af092be313f432b84918c7e1c436710839e404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `friendica:stable-apache` - linux; amd64

```console
$ docker pull friendica@sha256:063c95efe0df559bd87ad306dc862d1ce89e78553a984e1ed42917f8b0273ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259402621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21cb7353542520342f9bae3fee2f31e6aae7dcdfaacbf8ee4e753350c0c76d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Jan 2025 19:19:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_VERSION=8.2.28
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Jan 2025 19:19:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Jan 2025 19:19:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
WORKDIR /var/www/html
# Wed, 01 Jan 2025 19:19:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a6ce12b8d402dfdc199d5851a2114d895e954548837d8819601a221fae88aa`  
		Last Modified: Tue, 08 Apr 2025 01:23:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3348c51cdd76be25974ba13d21efea320335509df6355b7cd2730f213b01b35e`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 91.7 MB (91653859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e208a7f6a3efeed9fb5206ac888740254ed18770f5ba2ac8db6d90471b31c1`  
		Last Modified: Tue, 08 Apr 2025 01:23:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027ad41a9fc4e51a89da7bd16340ba58478bbb5c0a3b2c3eb9a15a5f20b99eba`  
		Last Modified: Tue, 08 Apr 2025 01:23:30 GMT  
		Size: 19.1 MB (19064234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca269e9e6c429e0dd196ac47427387ceb13a67df9838674f5e363020cd63af46`  
		Last Modified: Tue, 08 Apr 2025 01:23:30 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a0917f62c273f4e0ebc2c94b90f0739857f3eb7bca5fdd3bebca9df50cd6a0`  
		Last Modified: Tue, 08 Apr 2025 01:23:30 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fe2ca3844e64feb99cfb6c6367b57f9be0c7c3006fcffb565be79a35fb5cf0`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 12.3 MB (12273174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c0cfbb5ad923d2903c75b20b7baadc4dcf93ede73ef2e3dd63f5de3bf08975`  
		Last Modified: Tue, 08 Apr 2025 01:23:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd88255a1fd06ca751582a79755628f932c5fef71128e87c37d23b4bfe963e7`  
		Last Modified: Tue, 08 Apr 2025 01:23:33 GMT  
		Size: 11.4 MB (11354119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7072caf61c40107b5ba378a96754fa5c2908bc658c8a55cd518befca7cbd8b52`  
		Last Modified: Tue, 08 Apr 2025 01:23:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b1602159521e0664405180766704e4338c169bab56668f8f70fe1ffc1cc09`  
		Last Modified: Tue, 08 Apr 2025 01:23:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d335064f8ad8f1c34ceadcd1356ca538c05a4d495e4cf446edbb98d55f9301e1`  
		Last Modified: Tue, 08 Apr 2025 01:23:33 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9df9ea6b9d4d19d8672f6fce504c0a6cc733819bedceb586ab151f1f4b7636f`  
		Last Modified: Tue, 08 Apr 2025 02:19:26 GMT  
		Size: 15.8 MB (15764771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90ed08937104c55ff496925bce9c768f59efa7dfc63153eed08f8d8c2b90dd1`  
		Last Modified: Tue, 08 Apr 2025 02:19:26 GMT  
		Size: 1.1 MB (1122787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3366177cb28c3c204675821336a48d5ef19b37efc8b70d867a673dc4f438cf`  
		Last Modified: Tue, 08 Apr 2025 02:19:27 GMT  
		Size: 18.3 MB (18308351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929845644baa61e88bc7f35372c968eade62a39c8776a2a18c9913b0f0434078`  
		Last Modified: Tue, 08 Apr 2025 02:19:26 GMT  
		Size: 653.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c45382df1f3a670026c2550076272f8ec9bad74712a226b2b95d72e2ecf531`  
		Last Modified: Tue, 08 Apr 2025 02:19:27 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e1e85d0c820b8c7169008f1874eb3c3bc3b0f5ac8cb917b651b1ee83648373`  
		Last Modified: Tue, 08 Apr 2025 02:19:29 GMT  
		Size: 59.6 MB (59593140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151dd17085ced2afc1770a93635267a9595924d8f29a71017b1eee33e1231ce7`  
		Last Modified: Tue, 08 Apr 2025 02:19:28 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494cbb6f445b6b35fb052c5890412b23362f8abd71021bf0c6af68bb5c93d529`  
		Last Modified: Tue, 08 Apr 2025 02:19:28 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:ccbe4ab538c9882487b75e4b3cb23207a743c9904c81b90586a0e61aa674c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 KB (65461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24694188d1940f9154608006d689022428ffd78b0e052c6f778e9226e2359e2f`

```dockerfile
```

-	Layers:
	-	`sha256:8db1c83f75dd3d7c8eb32cb5c1c0a84d21d9e4ac9f9262f02b831a9046d8d7c7`  
		Last Modified: Tue, 08 Apr 2025 02:19:25 GMT  
		Size: 65.5 KB (65461 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; arm variant v7

```console
$ docker pull friendica@sha256:beb37468c744a5925fb2dc44b2947ed15f0e3acfcd674b1629429e928089356e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226086009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef619a6f080ad1e45f5e64353311c17e18d58c70901adf56c6abf1a83bf9487e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Jan 2025 19:19:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_VERSION=8.2.28
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Jan 2025 19:19:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Jan 2025 19:19:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
WORKDIR /var/www/html
# Wed, 01 Jan 2025 19:19:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bfc445187b87c4f640fe8b85c4ee3c251ce5e7023a5ff0acd053bde1f01e6aaf`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 25.5 MB (25539135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92905eaafdfcd979db495c58a48e731910176c26b376274ee7cb223a8c038a9b`  
		Last Modified: Tue, 08 Apr 2025 02:22:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b830cfc597b4f010f0ffe2c61b85171bd1913ba887acd5db1195c0f4451fc74`  
		Last Modified: Tue, 08 Apr 2025 02:22:08 GMT  
		Size: 69.3 MB (69324658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced68bec9de0dd3b531c6d6097fd77987a5e1401ad87f2c13daa930ebea5d07f`  
		Last Modified: Tue, 08 Apr 2025 02:22:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15cd11cd94a45d3f42639fe5069e8576f9c3f352afd3e318aa2eeee206f9e06`  
		Last Modified: Tue, 08 Apr 2025 02:25:52 GMT  
		Size: 17.8 MB (17817086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050fc544b8fdd7310c891ad6ba3e06deb200761ccbe5641d3103f549f3c0801`  
		Last Modified: Tue, 08 Apr 2025 02:25:51 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f480ab0c7e7dba154ce3b39509ee85942760d1affd46dc47a28e625198f925`  
		Last Modified: Tue, 08 Apr 2025 02:25:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3986b30a38506c84be1e75e28e8bec5956560d160ae8b4407bae218a54169a2b`  
		Last Modified: Tue, 08 Apr 2025 04:16:13 GMT  
		Size: 12.3 MB (12271672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e617970244d5c6d19aeb7a0dc984c42de07d531fdef2c751569d50a999ea4d7e`  
		Last Modified: Tue, 08 Apr 2025 04:16:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a9c233fc0faa38b85f469b933582fc9664983a06d2fc67e5a9928c10f181d4`  
		Last Modified: Tue, 08 Apr 2025 04:16:13 GMT  
		Size: 9.8 MB (9815992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c7c670e4b874b6375eb897afaf6c17c2b6f8e90c67f62a889cec5e549060bb`  
		Last Modified: Tue, 08 Apr 2025 04:16:12 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f293af009e3f1a1bb0a8fdc03de11c30c124e0b6f0cde06f0da2dfe5f126f`  
		Last Modified: Tue, 08 Apr 2025 04:16:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba88847476bc42ae670299af6eb5b8d7ec62df22ffe72482e717d0929241b8c`  
		Last Modified: Tue, 08 Apr 2025 04:16:13 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58f547e1e142222a3f00e799655d10b8d04343a6679d0a129dc8175fd1bdca`  
		Last Modified: Tue, 08 Apr 2025 18:07:27 GMT  
		Size: 15.7 MB (15728559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8457ac3864da07539c17dc25b6f426db393b086eee175034e3d83c1fd472fab7`  
		Last Modified: Tue, 08 Apr 2025 18:07:26 GMT  
		Size: 1.1 MB (1089290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609ee2f7df2d872d1fe0b55a4aed4f4a7047a1804ec860f7be8aae0c3d40e5a5`  
		Last Modified: Tue, 08 Apr 2025 18:07:27 GMT  
		Size: 14.9 MB (14897373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95affa9db64cb97887675e39bdff4d8749dfa0ef08cc5febb5d5d0b0f08ec2b`  
		Last Modified: Tue, 08 Apr 2025 18:07:26 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b961c7347546c4042e1662eec767282b3a0320a11dbf3a5dbf3e94f0c250dc07`  
		Last Modified: Tue, 08 Apr 2025 18:07:27 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2305a4ce57a1ee294fea6fdbbf3d199a505d92374dc007fc5ee97bd463cb44`  
		Last Modified: Tue, 08 Apr 2025 18:11:29 GMT  
		Size: 59.6 MB (59591456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb813b24220b4b8ff0efbc25b4b5b32ca31ca74caf1894b1744960b68ab93d7`  
		Last Modified: Tue, 08 Apr 2025 18:11:27 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065bebdc41642567a3f92bd37475bb82bff705441bb71f130545df41c1584d3`  
		Last Modified: Tue, 08 Apr 2025 18:11:27 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:8b4a01196cb7768b3843fc1febd7534b20ec59bdd0214e6de7c9ecc535ae8c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 KB (65608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7590e0c3d547d83f4cf430bf34490e87a2f1299cdd9d4d1e7c463c0c6bde2ce`

```dockerfile
```

-	Layers:
	-	`sha256:bfca643bcb2a736cc2d55a1a6da3ca5faca66d56aa4539e70b1c288af9cc098e`  
		Last Modified: Tue, 08 Apr 2025 18:11:27 GMT  
		Size: 65.6 KB (65608 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:201e8d03a821e0679e29228f3ab0e99cbb85e2b180830b87bb9b4e82ca769c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251110683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a78831ba0c9bd4ba895b1fcf5f7063ce6924a8fa1c4dceb153bc7aee8581aad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Jan 2025 19:19:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_VERSION=8.2.28
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Jan 2025 19:19:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Jan 2025 19:19:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
WORKDIR /var/www/html
# Wed, 01 Jan 2025 19:19:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f0196faf8027211a1d0ebc16dff39807ceef632e28a2806370d0afa31a0689`  
		Last Modified: Tue, 08 Apr 2025 02:34:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee195fcb6391fc3b303daebb47384a6a7295ddc385d499c1db5c640963f9ce5`  
		Last Modified: Tue, 08 Apr 2025 02:34:31 GMT  
		Size: 86.9 MB (86940199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafb03c0089cab248fb128a84e21004401b5901950d28bfe8f3b9deb5b935348`  
		Last Modified: Tue, 08 Apr 2025 02:34:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69d2d6c4c3e70c459369537c8f9d78c4a57eebd255818e814a8f57461baccf3`  
		Last Modified: Tue, 08 Apr 2025 02:37:48 GMT  
		Size: 19.0 MB (18981606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a8522d49033253647764545cca099c7e9666db43f7ccebc825b7b274f7d82`  
		Last Modified: Tue, 08 Apr 2025 02:37:48 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cbbe7eb68e64dba28c75e305b819aae7a47033af894903e00b3baebfb83f20`  
		Last Modified: Tue, 08 Apr 2025 02:37:48 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb51d1fc44427a6af7f1316d0dc858a0d4e0e17adf38e42e3ae7432decc846f`  
		Last Modified: Tue, 08 Apr 2025 04:44:37 GMT  
		Size: 12.3 MB (12272518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91140831a24daac304a5ed9d76232f30f77da8861b65e2d361ccb8af4dec894b`  
		Last Modified: Tue, 08 Apr 2025 04:44:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff8bd3f08fda46f1f60b754a79606f7c4572456cb9a31729c18eff2246bb66c`  
		Last Modified: Tue, 08 Apr 2025 04:44:37 GMT  
		Size: 11.4 MB (11441629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af4a51c2cdb91b7bb62adfcc4dd222448f23dcda9dea27e42c6963ce1b3e944`  
		Last Modified: Tue, 08 Apr 2025 04:44:36 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82175df561cbb17701b53b00b784b6a79eb8fa1dc7bfcd1b974ae5004caf6f61`  
		Last Modified: Tue, 08 Apr 2025 04:44:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def5f69ad2d896807c313ea74efd021417d3f8685e983e541647f12f77917cd8`  
		Last Modified: Tue, 08 Apr 2025 04:44:37 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c959d68f85b38dfa8beded85df3a0c52833785ad606fbd2cfa46286c1be4a502`  
		Last Modified: Tue, 08 Apr 2025 13:00:28 GMT  
		Size: 15.5 MB (15526367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271d50a75c44939eeb0d66b78962f1bf08e8979fac4847b997021694004fb2a`  
		Last Modified: Tue, 08 Apr 2025 13:00:28 GMT  
		Size: 1.1 MB (1053888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd5bc920ad22d77bebad577d409d327561a71f5a5beaf11f00e806d9f0ec6b3`  
		Last Modified: Tue, 08 Apr 2025 13:00:28 GMT  
		Size: 16.5 MB (16541551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c679c771979898fe7be05beb42acdf1cfe8ffdaa41356d2801e77f41e1cf2140`  
		Last Modified: Tue, 08 Apr 2025 13:00:27 GMT  
		Size: 656.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa50df94dfb636a4d8098bbf7d63ad939c5b29d03831696c2cfcbe8d137d2bc`  
		Last Modified: Tue, 08 Apr 2025 13:00:28 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1948c970eef5c305c5350df8bd5fa9fa63b9f0b5ad11cd03599334cb3ef0877c`  
		Last Modified: Tue, 08 Apr 2025 13:00:30 GMT  
		Size: 59.6 MB (59592639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37965571d824fa37220c9531f9e3e6c5324a24e80f9bc1cdd0e443c338a2aa76`  
		Last Modified: Tue, 08 Apr 2025 13:00:29 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069e27178b9435f2bbbc726f4fa65baaf2fa07c08f0493ce0032e097f951a3f`  
		Last Modified: Tue, 08 Apr 2025 13:00:29 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:70cc7304bd2c07345a86dfe01789f4108d4382eaa8bcbb14f5ab95b3c94a4d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 KB (65664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3334707a2e550b2d91e6fed7289e6f1d24b8dff160c5b848c7a876993c8ed0`

```dockerfile
```

-	Layers:
	-	`sha256:cc08ec83ca2c746d15849c32d7758cdcc4e89ef7add9f34ebb1afa413393a6a6`  
		Last Modified: Tue, 08 Apr 2025 13:00:27 GMT  
		Size: 65.7 KB (65664 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-apache` - linux; 386

```console
$ docker pull friendica@sha256:65202108d57747edfa1560f9f0400f8542194010c2497570d6cd1bd86d6950db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261844049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b59857966b55a2924350e2e71d36ddcf481bb557171073905e1a041eabc8be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Jan 2025 19:19:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Jan 2025 19:19:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_VERSION=8.2.28
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Jan 2025 19:19:24 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Jan 2025 19:19:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
WORKDIR /var/www/html
# Wed, 01 Jan 2025 19:19:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
VOLUME [/var/www/html]
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_VERSION=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_ADDONS=2024.12
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Wed, 01 Jan 2025 19:19:24 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Wed, 01 Jan 2025 19:19:24 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Wed, 01 Jan 2025 19:19:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Jan 2025 19:19:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba1bf752b995d5955dc4271175171a5577e443f3279292148323850e92cc3d0`  
		Last Modified: Tue, 08 Apr 2025 01:23:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9679872b13faa491f0f7da222d7cd3f28d13eb4dc209939e24f02e7e557b1ec`  
		Last Modified: Tue, 08 Apr 2025 01:23:40 GMT  
		Size: 92.7 MB (92724865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fcc5ba1b31df3809cf0886f63b12f671fc9d3223f0393d67d6ce79a68a2bc7`  
		Last Modified: Tue, 08 Apr 2025 01:23:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f14f3a4bc02ca735eaa9014e32171f770c19168d04268c8116beb2755713159`  
		Last Modified: Tue, 08 Apr 2025 01:23:38 GMT  
		Size: 19.6 MB (19552870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28125a1735c348326e489ef2856e4608e9993aae62ed22252660dcc61b27348a`  
		Last Modified: Tue, 08 Apr 2025 01:23:38 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5ac16f86552d8e8a1218909cd94ca801c1aa66e41bf735d890cb043436649e`  
		Last Modified: Tue, 08 Apr 2025 01:23:38 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3820297a2c0672d569aa7582ed91082b519d0dfc9d016b5d6208aa4bfe5c3e96`  
		Last Modified: Tue, 08 Apr 2025 01:23:39 GMT  
		Size: 12.3 MB (12272500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac12c71d8f6a0ef9c9f876f253405a1501139f2b5e7795dbc329012591236e5`  
		Last Modified: Tue, 08 Apr 2025 01:23:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0079957525d4afd27d78e5ba0bb8672f39cd2883faf24d54772f0412062bcbf`  
		Last Modified: Tue, 08 Apr 2025 01:23:40 GMT  
		Size: 11.6 MB (11599546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b954c8a390331dc57333ab564e95ee1b870cff172d6232592cd1174522ee35e`  
		Last Modified: Tue, 08 Apr 2025 01:23:39 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f71721bf04c9a50bd08eb321d9250b9ad14e9eadcf8d5ac737c9190bc34c6`  
		Last Modified: Tue, 08 Apr 2025 01:23:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8eed057f16093e044bbce875e62c54ff5d2784629e1484a302b95183e7666`  
		Last Modified: Tue, 08 Apr 2025 01:23:40 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfda53fba764806a5e3eb6e597ecf406806c6be33747a523d4422f2d9701d7e`  
		Last Modified: Tue, 08 Apr 2025 02:19:01 GMT  
		Size: 16.2 MB (16238242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5abc0217a7fc07638b26a00fe150dde952bf34d8011dbd6df851171d8cfa001`  
		Last Modified: Tue, 08 Apr 2025 02:19:01 GMT  
		Size: 1.1 MB (1096657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df24c3aa898467bbf0fff25d411b1d9f9f301c6ffbf69f6e7514480f64e8e16`  
		Last Modified: Tue, 08 Apr 2025 02:19:01 GMT  
		Size: 17.6 MB (17571670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4add42b91b64e804112e89344d7340070956fe4c1bb2a4627d9c7f78f1d79b`  
		Last Modified: Tue, 08 Apr 2025 02:19:01 GMT  
		Size: 653.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2bf64b1ed3eec1106690acd1bbdd35a65ec654bc461848ca056ee82b0aca80`  
		Last Modified: Tue, 08 Apr 2025 02:19:02 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f3c2dfb5e31b509514a81d421e03f6464ec6c77133d5ccf9c91b2c2ee553cd`  
		Last Modified: Tue, 08 Apr 2025 02:19:04 GMT  
		Size: 59.6 MB (59592352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c812ae03c33bd6be84818646afd0f25e5d43fd45ae5589125d46d7b5feebdbf`  
		Last Modified: Tue, 08 Apr 2025 02:19:03 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e3452c2e2b6e4c9fd1dfb7ac7f0d96160fe04883bcd1cf415ce3964e646841`  
		Last Modified: Tue, 08 Apr 2025 02:19:03 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-apache` - unknown; unknown

```console
$ docker pull friendica@sha256:2d9ebd7c19c5c370b7a738d01767e24196d861c02e623d893e96e1be18a897d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 KB (65409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d8d186c990655d00e017e82afb287c85a4bf913e3795929c3037a129a1d6f2`

```dockerfile
```

-	Layers:
	-	`sha256:6701a71fec69b83a7f1e260849f0acccced35a5fcb5594d03253bfc4899bb215`  
		Last Modified: Tue, 08 Apr 2025 02:19:01 GMT  
		Size: 65.4 KB (65409 bytes)  
		MIME: application/vnd.in-toto+json
