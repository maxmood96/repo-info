## `friendica:latest`

```console
$ docker pull friendica@sha256:75e0f50c8eeeb5c9f4a0dae887f5e12fda02329a08feaedd8945ddf60be37408
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

### `friendica:latest` - linux; amd64

```console
$ docker pull friendica@sha256:6a5d447cc24447892f7efa39099e9a72dcb938c9889fc60c9a9a4b974ca86005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254290654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1d2f5037fa26db7937345df999d739b66c849a2592a475811c660770e35add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.30
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGWINCH
# Mon, 19 Aug 2024 01:45:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GOSU_VERSION=1.14
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
VOLUME [/var/www/html]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_VERSION=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_ADDONS=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=3e93178734bc82abd0c7c8b8b7c13baa4c18ae33a0f07c169518c13c4317717d
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=748d399f64670e37a5afc94ef65483291c52e9374e26c0ee5235f91b55449f54
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc18de7bfbb69fab1244f1b06a4ed23a27a914b6096f17140dc5ba564ee7e518`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e5896b98ee8ceea0ce7e959b6c0459a19549427e50a2e078aff431cb0bcb43`  
		Last Modified: Tue, 12 Nov 2024 02:10:53 GMT  
		Size: 91.4 MB (91448630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046efe3318e46200cf36665a450d0d6ca3fdf0fea01b69745d572ccd79768482`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6985708e5a0a663b411e07c1b532206fbd8dfd75aedc4a421bc6d84eb68567`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 19.1 MB (19064324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117bfc0f7c0f63e91ebddadd1f2ad41d05fcef8c048ddf3297feb39dfb6827cb`  
		Last Modified: Tue, 12 Nov 2024 02:10:52 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a2bed7375a273662b0e8a30bc14909d36344b47a53b9d371203fc2d123ea5`  
		Last Modified: Tue, 12 Nov 2024 02:10:53 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c6b4283c5d791c13f2eb32823b946a45fa7c57ef6ffe5024be004196ab0fa`  
		Last Modified: Tue, 12 Nov 2024 02:10:53 GMT  
		Size: 12.0 MB (11975594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166a681dcce956dadef9db30a8ab7491698ff346508471fee826a414a56ace5e`  
		Last Modified: Tue, 12 Nov 2024 02:10:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854e532c8dc89e6a43522f76be7f519c749b21b82d260904af24199d627a4f8a`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 11.1 MB (11083476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccebf52e1bdd0b08b23f3b313bf5086fb2cdcf51e48cbc99c0c9f361c942f859`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62126214130b2e3017a166f3b7aa0ab56f5fb1731d2df0c1dc62cb8e0ff6de`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725aae3b69468ee9fef4df12c37a3f7fb5bcd6cdb2bb276b348c4764eb3f8854`  
		Last Modified: Tue, 12 Nov 2024 02:10:55 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01e0d56b9a6cf73863ea90837ea534fa44a2a975678325e0be3eb65cdefacff`  
		Last Modified: Tue, 12 Nov 2024 03:09:42 GMT  
		Size: 15.7 MB (15679753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49fbc0eb37b0f90365dc9aec09e56b0f4a8e3fcd022d28c91a20ddcefbabf4c`  
		Last Modified: Tue, 12 Nov 2024 03:09:42 GMT  
		Size: 1.1 MB (1069402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ba1e8de86f4dceb26e197d16b5276f745312947fe3d631abc86d13d2bc7181`  
		Last Modified: Tue, 12 Nov 2024 03:09:43 GMT  
		Size: 18.2 MB (18199790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acce76297eeb8c270833018ab39ae83627ec754fcdc055bea0e8544791961671`  
		Last Modified: Tue, 12 Nov 2024 03:09:42 GMT  
		Size: 649.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e86f73cf0861f04354178ef9e4e99d4a17c1a23b685c7d96938b9af7bb0c0b`  
		Last Modified: Tue, 12 Nov 2024 03:09:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c90d25a2836bd3120d2a114f2cf4f22cb911b20e027a3be7a0bf295369875d`  
		Last Modified: Tue, 12 Nov 2024 03:09:44 GMT  
		Size: 54.3 MB (54307355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193732e5e25fd2146119fc8de39c0c3aed3992f32d353dbbf9f9dff2f9a5b33d`  
		Last Modified: Tue, 12 Nov 2024 03:09:44 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bb6d5a889b0cc14eeadfd9e4a4fb04a4b0469e5fd4a2df1c2c317905b10aa7`  
		Last Modified: Tue, 12 Nov 2024 03:09:43 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:c634d4ce56c67f1b198339d3efab1ad211ca8260c3be44f9ce12a80d8a711ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 KB (65290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500fb0e73b5f8d28b1e13b202df1286e62e27ae783111e999a176ca65d366970`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ae86b2f49601d3023e52db29c1ee712a813bc90526bd2c0d01bded8594635`  
		Last Modified: Tue, 12 Nov 2024 03:09:42 GMT  
		Size: 65.3 KB (65290 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; arm variant v7

```console
$ docker pull friendica@sha256:bf8697767cc8c404ab44dd6394814ff4389d78845602383bdf8226c1b04cfa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223400230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc2ab303a7e5bf6fdd758c5b4c1a9c2d629bb0aa2fba902b3b229c14ebab5cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.30
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGWINCH
# Mon, 19 Aug 2024 01:45:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GOSU_VERSION=1.14
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
VOLUME [/var/www/html]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_VERSION=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_ADDONS=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=3e93178734bc82abd0c7c8b8b7c13baa4c18ae33a0f07c169518c13c4317717d
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=748d399f64670e37a5afc94ef65483291c52e9374e26c0ee5235f91b55449f54
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337fe7adf8bb0c30412a7fd274c70a1d661f98880e77a67bac6803fb70a38309`  
		Last Modified: Mon, 28 Oct 2024 22:28:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6190e3d66b99aba4c02b38893eebd4bc7cda871fb4a8df549a407a97b5ce536e`  
		Last Modified: Mon, 28 Oct 2024 22:28:14 GMT  
		Size: 71.4 MB (71401429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399bb0bff9627b1d44be3d8b5c1859b2b555601a37f98fe76d871c0dd8ea1826`  
		Last Modified: Mon, 28 Oct 2024 22:28:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84c58a7f6bb9ad79fadfbf526c7adc5e0790a56940fbab3b02f08c153d00109`  
		Last Modified: Mon, 28 Oct 2024 22:33:56 GMT  
		Size: 17.8 MB (17817140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fb3166ecfd24165f779a0464dceed8c47da877f6608fb4172ebb8ace14fcbf`  
		Last Modified: Mon, 28 Oct 2024 22:33:56 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c92e1ba3ce366e82499a10cd7c3b6f0c14059546a06a4e284136a417fa3290`  
		Last Modified: Mon, 28 Oct 2024 22:33:56 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c802c89abbb590a254ec16b3de01164ec2287e067673473ba5a04e60be92bc2d`  
		Last Modified: Tue, 29 Oct 2024 01:25:55 GMT  
		Size: 12.0 MB (11974431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca905f56d3ec5469ab903f0240e10ff08bebd3e09a4f2f235841d96af5f8019`  
		Last Modified: Tue, 29 Oct 2024 01:25:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b45e9ebb774e11d387de76965ca546febf66e970e038f2457183ec82cef0f3`  
		Last Modified: Tue, 29 Oct 2024 01:25:55 GMT  
		Size: 9.6 MB (9568221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb613d88fccecf21410a4c27c2ce8d573a9b2938df53c0ac78ea5be638b7b1a2`  
		Last Modified: Tue, 29 Oct 2024 01:25:54 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40544396bcb7d9489ad053bfc36845b00f3a92e7db6f451263b66b8bef0d7b78`  
		Last Modified: Tue, 29 Oct 2024 01:25:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9209d27e576802a608e9dd8dcd5cf606c086c96162d1e0fc8552faaf6c5df061`  
		Last Modified: Tue, 29 Oct 2024 01:25:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afbb7b722e996722752f0128e7612dbcd84342dd982246cfb75b6a5f19820f6`  
		Last Modified: Tue, 29 Oct 2024 02:48:00 GMT  
		Size: 15.6 MB (15637632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091f776931457ccabc106dbcf77750bd94054ccb50c8c83ce411ed4f15752f84`  
		Last Modified: Tue, 29 Oct 2024 02:47:59 GMT  
		Size: 1.0 MB (1024246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2d706ca1e64a9f4d3dcc5846a4ad6f30f56135b0b160e104a8dd59347b01ec`  
		Last Modified: Tue, 29 Oct 2024 02:48:00 GMT  
		Size: 15.1 MB (15070759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905fda4bc1bccd1e4b4a25d335288831e4bb9d1a39495abc426832382e8a7536`  
		Last Modified: Tue, 29 Oct 2024 02:47:59 GMT  
		Size: 654.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e1ae4eb9add11f244525ec78176dd90303203335719062c63e57f1bcf5570`  
		Last Modified: Tue, 29 Oct 2024 02:48:00 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117c77e41854cf65ee2d7e2ebe96f9d9054bb797500a79f346bf752c41542859`  
		Last Modified: Tue, 29 Oct 2024 02:48:02 GMT  
		Size: 54.3 MB (54306036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695d10a109237190d154502f464d2889c54a1d2defdeb6d23005bd7c029fe91e`  
		Last Modified: Tue, 29 Oct 2024 02:48:01 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2180185bb4d13925e546b17cf42524450460f4a77beb06007917056a1aadbae`  
		Last Modified: Tue, 29 Oct 2024 02:48:01 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:4b82bfd24a01a4b19ebc90758174c4939fe1f32dd7b9da930283a72ccaeb1f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 KB (65492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fea69899405f7c3c4f361a0d20f6b97fe17c701cf764bd79a1141b255b45da`

```dockerfile
```

-	Layers:
	-	`sha256:8bede45141c5f83d5fcd958245d255d5b736bb3b8a50042e364e5443f6a92323`  
		Last Modified: Tue, 29 Oct 2024 02:47:58 GMT  
		Size: 65.5 KB (65492 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:286d60548d0086cada5e07b00cf3170e3cf57c563d67e81def560ba434300e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248848334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac5697a7fca6183bceaffc4568c44f937252d3d23e2cf79fedbfc4e906da2cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.30
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGWINCH
# Mon, 19 Aug 2024 01:45:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GOSU_VERSION=1.14
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
VOLUME [/var/www/html]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_VERSION=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_ADDONS=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=3e93178734bc82abd0c7c8b8b7c13baa4c18ae33a0f07c169518c13c4317717d
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=748d399f64670e37a5afc94ef65483291c52e9374e26c0ee5235f91b55449f54
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53690d62b043432dffaddbde5b238e5476a1322598b8fec4beb77859d2b27`  
		Last Modified: Mon, 28 Oct 2024 22:17:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8813bf005525af380dc3d44872218b6536729556fd964b34b0835a8f7ee962e7`  
		Last Modified: Mon, 28 Oct 2024 22:17:40 GMT  
		Size: 89.2 MB (89157168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec391378bef083f50fe902a630be5ce7458250870af03404ab3110c1037287`  
		Last Modified: Mon, 28 Oct 2024 22:17:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12fbe9e3ef4405baa851a287bfcd6cc85f8ba3454a6d71820ac5ad0ea70eaec`  
		Last Modified: Mon, 28 Oct 2024 22:21:00 GMT  
		Size: 19.0 MB (18981262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432299646c17b28a002666344dbfd2aff2cb8dda6ad7bc14d599e96df49e43ff`  
		Last Modified: Mon, 28 Oct 2024 22:21:00 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a91506317031b742d1a60c84f4c090f8feb6b7fd453329f5eb84fe6e280dbc`  
		Last Modified: Mon, 28 Oct 2024 22:21:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2851383623a47e1c9a4cab5ad8dd4173818bd4835dd41877273e56fb416c3a2a`  
		Last Modified: Tue, 29 Oct 2024 01:13:01 GMT  
		Size: 12.0 MB (11974992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a50e2bc91cf7d28874ee1a1b8fa86ff68415eb45e998e5713db8aa447e0317e`  
		Last Modified: Tue, 29 Oct 2024 01:13:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ce90857da755e14cece6d47a0b5aa911142484f91aa441cc35a9079428558`  
		Last Modified: Tue, 29 Oct 2024 01:13:01 GMT  
		Size: 11.2 MB (11150959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1976b59447e41394356a0c91e87ab7a5d4d255dda2d6bbe24a8f11b5f5bdfa`  
		Last Modified: Tue, 29 Oct 2024 01:13:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd64e4347f6c0d476b8b874709b2bf6a7024e9e3683ca71a6c56e03ed739d707`  
		Last Modified: Tue, 29 Oct 2024 01:13:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27bd04b6b3c8109cc96724c2e2be203df68900401ae729aa78550510959762`  
		Last Modified: Tue, 29 Oct 2024 01:13:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ceca32cd922ec049e6d5af582ce4f8c45f3c6f339fadd789d2bab09aec6ed`  
		Last Modified: Tue, 29 Oct 2024 03:02:57 GMT  
		Size: 15.4 MB (15440177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc117aa77a72ae93721264e133b99ca72afb133f3ca5c4737954d1389bfe80d`  
		Last Modified: Tue, 29 Oct 2024 03:02:57 GMT  
		Size: 996.6 KB (996595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963382115cd5ff98325ec0e7d64681534fa72715ea28f00675fb7438e7a8c007`  
		Last Modified: Tue, 29 Oct 2024 03:02:57 GMT  
		Size: 16.8 MB (16753553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8862ffc3bc78cb1b9f989c210dd2d57da719441f8d9f4ea97bff209404cebe1`  
		Last Modified: Tue, 29 Oct 2024 03:02:57 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a09941bc4ee30fdb22a630cf4a82f42a8515009c21e75e2763192b19f9762`  
		Last Modified: Tue, 29 Oct 2024 03:02:58 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9203832009e826827bb81937ca02ba4f93adeae11969872f003e341ce7c502d5`  
		Last Modified: Tue, 29 Oct 2024 03:03:00 GMT  
		Size: 54.3 MB (54307100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b337562b73a253445113bfd3f827d3546feb8dcf6cf7f2aa7883303461af751e`  
		Last Modified: Tue, 29 Oct 2024 03:02:59 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b7dbbcab4897115018a70178c14259a12954992bcee6fb5314ec4f12ae25b8`  
		Last Modified: Tue, 29 Oct 2024 03:02:59 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:9d0255c08c70eee9ab31359a746958240d58af40fe0e525a9f95fe68c3e88989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 KB (65540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e69be20ce9d2454045a762cc207d0d606ea7f446d6a1b079f51838c2830c4b`

```dockerfile
```

-	Layers:
	-	`sha256:ba278a137c282b486e7eafac9994092cfb8a89134e77c56a95e2bd9c305b1eb7`  
		Last Modified: Tue, 29 Oct 2024 03:02:56 GMT  
		Size: 65.5 KB (65540 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:latest` - linux; 386

```console
$ docker pull friendica@sha256:317649070410f0d335d737e37fb93613a45d3a4bb777fe97099f1410ef466f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256755521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d83665a5e8c38bafacd6279dd654092aa41ecc61dfdff3a44c126557f29e531`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 19 Aug 2024 01:45:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.30
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGWINCH
# Mon, 19 Aug 2024 01:45:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GOSU_VERSION=1.14
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.23;     pecl install memcached-3.2.0RC2;     pecl install redis-6.0.2;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
VOLUME [/var/www/html]
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;    a2enmod rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_VERSION=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_ADDONS=2024.08
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=3e93178734bc82abd0c7c8b8b7c13baa4c18ae33a0f07c169518c13c4317717d
# Mon, 19 Aug 2024 01:45:21 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=748d399f64670e37a5afc94ef65483291c52e9374e26c0ee5235f91b55449f54
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc             "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f88b2716ef49709b180ab9aa00ccefba0b574361b28b66c0b08f2ba48b5de`  
		Last Modified: Tue, 12 Nov 2024 02:10:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb7ab0d5d10903f84b43acf6f8bf064968263ddad1c377353a4ab5e9bdb8781`  
		Last Modified: Tue, 12 Nov 2024 02:10:59 GMT  
		Size: 92.5 MB (92521332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cd9a1e42d2bbd5c63435ad38f36834573aecc05b0bb5be986ec1dcea563fe`  
		Last Modified: Tue, 12 Nov 2024 02:10:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077d28b8afe2738eb7c97ae3f65ab42fe23615a99c065a1d4a689fa578e5ce05`  
		Last Modified: Tue, 12 Nov 2024 02:10:57 GMT  
		Size: 19.6 MB (19552830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95df20383c508f6269f0c675358b01bfb34516645df7f2216a23460af613ea45`  
		Last Modified: Tue, 12 Nov 2024 02:10:57 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7058be1edaabf80c910839997a9953d0d6fcf6c95e2b6c9ab1fcd8081f6ab6d`  
		Last Modified: Tue, 12 Nov 2024 02:10:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfea493180a8c372c87e5d9db57913da40600ff26da8af12d9568166ff9409b9`  
		Last Modified: Tue, 12 Nov 2024 02:10:58 GMT  
		Size: 12.0 MB (11974859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f18386502c5c8e567d895451a8df216a0903bde0e59a8398ebdba106afa8d8`  
		Last Modified: Tue, 12 Nov 2024 02:10:58 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f392269fb1e28d94e583a7dd7a99638629b96494f132f9cac2b7e68790f183b7`  
		Last Modified: Tue, 12 Nov 2024 02:10:58 GMT  
		Size: 11.3 MB (11315390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb500d0ac4230f4bc48fed7f4496dd8e8c7b39aee88bfbbda8b4b9139928902`  
		Last Modified: Tue, 12 Nov 2024 02:10:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b064b58c0ec77b46412e7e93cadbf7b15c3acb84e2be9f7f4867be310a552313`  
		Last Modified: Tue, 12 Nov 2024 02:10:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa02690344ee64e5a7f587563d9f8565a4be38e262c5e40a2f59b399275ea1`  
		Last Modified: Tue, 12 Nov 2024 02:10:59 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450411055a1f98e8fa9caf1753569acc2d2e889abca6913a21a5a4438776f192`  
		Last Modified: Tue, 12 Nov 2024 03:10:16 GMT  
		Size: 16.1 MB (16149445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cde2ad7ff6d7ea25353b22388c130deec146051794936d702e3a6277d73901`  
		Last Modified: Tue, 12 Nov 2024 03:10:16 GMT  
		Size: 1.0 MB (1036141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16db7e066f8da39d59e882e15e56fdaa48bf0fdd5dd30dabd0d52f080ebccc77`  
		Last Modified: Tue, 12 Nov 2024 03:10:16 GMT  
		Size: 17.5 MB (17464905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f4926e32c9ce1a674d265e5367e99855e723f60cecae6569cd0e7bc5164a2f`  
		Last Modified: Tue, 12 Nov 2024 03:10:16 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3fbe4119a85ab23d7abd5dddf413a8319160759911ab9a7d031d1bd238e87e`  
		Last Modified: Tue, 12 Nov 2024 03:10:17 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddba7762775994c0677bc970513929ced4a83983b2b91639d3ad61ad15450290`  
		Last Modified: Tue, 12 Nov 2024 03:10:18 GMT  
		Size: 54.3 MB (54306500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ed36c3a7f9a0a85f2edc82b523ffa5d299418111119f7549b9e4fff67687aa`  
		Last Modified: Tue, 12 Nov 2024 03:10:17 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f1e22da5975cf7b8578d373f13bded10e75ccbdde97f950db98305c8c06c1b`  
		Last Modified: Tue, 12 Nov 2024 03:10:17 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:latest` - unknown; unknown

```console
$ docker pull friendica@sha256:0917f95acd48dc4fc065c5bdb2f09d1ed34b6dd7bd4ed3c3a63199b10f4d5551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 KB (65237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcca78c6bd525e78a506ba6fe19c9502d1d339d816f9ea2ea9b6df3160a3e899`

```dockerfile
```

-	Layers:
	-	`sha256:419cac85157f25ff40eb77c67d1ed7fac00b69c321839e89d89fc5bfe164e708`  
		Last Modified: Tue, 12 Nov 2024 03:10:15 GMT  
		Size: 65.2 KB (65237 bytes)  
		MIME: application/vnd.in-toto+json
