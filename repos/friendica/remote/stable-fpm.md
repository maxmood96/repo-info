## `friendica:stable-fpm`

```console
$ docker pull friendica@sha256:adb974b0ca44b5f1d88c47e88aba10ce49b6fce1e511bb8606b38ea3b1629a9c
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

### `friendica:stable-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:f1702708ce9a354e68eb133c7f2c9d8eae9cb55543b745432d0ce246ff2f2222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249105514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e52e7b03864c24e2e08711797016c29c0214cc7aee263b88ed5adc9a1b5712`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.31
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["php-fpm"]
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d8ae96127a2ff8ab56a33d4f568c4e669749042fedc978f4c9b6ea76a05259`  
		Last Modified: Tue, 03 Dec 2024 02:29:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83e1239aaeae64bf7c2e3bc0d21356c3ba263478d6098f1d192765b4f0e4c62`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 91.4 MB (91448658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40797246c3921ecb3ec4b78bb344b8ecbe1e5e784fcffd92c75c6336f3cf91`  
		Last Modified: Tue, 03 Dec 2024 02:29:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c209741672fc6d0af87e39a59ff0f01cc1385fb85ef8bc701b14cd4da6f062`  
		Last Modified: Tue, 03 Dec 2024 02:29:15 GMT  
		Size: 12.0 MB (12020200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5f9e482b87e99bc59147d4be38d83541d282f388588990c7811ce5296329ad`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041393c99337780b691ddf907bc29729cd07a7a671a8c5598da8c44d34e17d44`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 26.1 MB (26054418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b6410731163ebca2dadf4403530ebddda832d264471c160f614d7166c20639`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea19b8f16e7b835a9c6d64160eef4175200e430d8230a15e7d2cb5dd8e543ae`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7171fa6bd4d670a6377b980bc7b83eb6f0bbae41ffeec0ce6022931870ff630`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7fc92e4cedf007bb7f9040c8561b720f9d38d63e82d05058beb281b5aef85c`  
		Last Modified: Tue, 03 Dec 2024 03:24:18 GMT  
		Size: 15.7 MB (15668382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ab24a80e1d2975a69a581ff6fc601196d7e9e92161d0e05c942fd8ca6ea9aa`  
		Last Modified: Tue, 03 Dec 2024 03:24:18 GMT  
		Size: 1.0 MB (1042579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a649e7856b9e522fa64e4daa63648d430f2d1cd5deee01f2a13e6bb0db92094`  
		Last Modified: Tue, 03 Dec 2024 03:24:19 GMT  
		Size: 18.3 MB (18318385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2cece2ae5ebf780a58607d63abdeca503c33334a98d4d365afabce1197ea65`  
		Last Modified: Tue, 03 Dec 2024 03:24:18 GMT  
		Size: 651.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602ecb56ed99db348061cd8451c3d634a9ab8108c50801fe5808e93a28b4a47`  
		Last Modified: Tue, 03 Dec 2024 03:24:21 GMT  
		Size: 54.3 MB (54282950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec08f51e28b03bb809b3a75e1cfed405a7a671a897b30437818e3074c251f45`  
		Last Modified: Tue, 03 Dec 2024 03:24:19 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa491acbb53123cc14aba53c11d45844312a99f6ead81f557b91f901751b8644`  
		Last Modified: Tue, 03 Dec 2024 03:24:20 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:d4a31a510bf7fa1abb37f6e1aa712fc7132dfd7fd6cb006ca0799182d7718e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 KB (54418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb0c4dad64bd8520201a71390502a0ec5358f1b63136dc632024cbc1a97f67b`

```dockerfile
```

-	Layers:
	-	`sha256:35815c55a1868e83c9aca5c752110e2f7f7e658918760a07e6bc1b81e8491f86`  
		Last Modified: Tue, 03 Dec 2024 03:24:18 GMT  
		Size: 54.4 KB (54418 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:91570349c1f9fb10356ae1748836a373c90a05d99dfe39291f1e8920be2abc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217716516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ed8bb37aba9accbcc6609babc7d9aabbbf3e758465b56ac24ffe1216258c07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.31
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["php-fpm"]
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8516b12615a3e7a2a821bfa14ba9dd6f6761aadf1ebf4642a203f52c8e3818dc`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7345669dd3937e5ef95133666ed38ccd4ce9f43d25a81fc19533223b2f1211ab`  
		Last Modified: Tue, 12 Nov 2024 03:32:45 GMT  
		Size: 69.1 MB (69119360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef234fa44e31ba745b124f418b0d1419fe927ae1ee59212901e32e4379c7b7`  
		Last Modified: Tue, 12 Nov 2024 03:32:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db098438c141f4e975eee7f5b767dfdc03dd41068c25683c15d6ffbd9ab792`  
		Last Modified: Thu, 21 Nov 2024 20:47:59 GMT  
		Size: 12.0 MB (12018916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0770953c9782e6b86a2694be97c5c7ce4d41d1ccbd44a79984f2656868da0e01`  
		Last Modified: Thu, 21 Nov 2024 20:47:58 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919f4e36940f5cc48bca52e4877be8ce5e40e6ee536362d560e25772a0595c63`  
		Last Modified: Thu, 21 Nov 2024 21:01:46 GMT  
		Size: 24.2 MB (24182728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc87fa4227c5e2f034e72241673828a6614495e68db81d773b65dc82131f561f`  
		Last Modified: Thu, 21 Nov 2024 21:01:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766a07f85a8d5349c346adcfd754f587d6d53bed411ee0a6bac6b130b25552ea`  
		Last Modified: Thu, 21 Nov 2024 21:01:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da21574efd4ffdb8421cd0bd96da0dedeac4d2ab67ae07a02e5f8433a8130710`  
		Last Modified: Thu, 21 Nov 2024 21:01:45 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f411e99fb98b5d09e34a50b181ef6b8c365ae07f01408ac94f35bb52f4cbcdf6`  
		Last Modified: Thu, 21 Nov 2024 23:15:38 GMT  
		Size: 15.6 MB (15614886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fceace8e9517a7c328823c60633999e6b7ad47c68bb7869980583274afe0adf`  
		Last Modified: Thu, 21 Nov 2024 23:15:37 GMT  
		Size: 998.1 KB (998149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce2c18e09facc5f35037857ceb577ed7ff6af386160185f93e401be62c1c45`  
		Last Modified: Thu, 21 Nov 2024 23:15:38 GMT  
		Size: 14.9 MB (14874372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafd49e39f0c517661d6aa151b273d1e756ed3ee81e5c74c82b2b5d64d1a8366`  
		Last Modified: Thu, 21 Nov 2024 23:15:37 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadf3f260846e048271385494454a7fa368682720ee46cf313d68375b8a16aed`  
		Last Modified: Thu, 21 Nov 2024 23:15:40 GMT  
		Size: 54.3 MB (54281530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8276f3f4288aaca32931bc63761d0797bb2ea0f276ea53090a9ab19aa4c50b2f`  
		Last Modified: Thu, 21 Nov 2024 23:15:38 GMT  
		Size: 3.2 KB (3181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e189e6249da85bd4c01e73e6692c7d5bc3f073d592389cefb8e86a97a1ce99dd`  
		Last Modified: Thu, 21 Nov 2024 23:15:39 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:3f5b3745e49ea7f01702a00587c093152afb9fa9546a815c6432600a8ac0f881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 KB (54532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f9b38dcee34f5afdce324ac87155c592957f54bdeb333db5a6a5afb710d50e`

```dockerfile
```

-	Layers:
	-	`sha256:e19aeef0566279f4a70948929e81279410f89f4ceb9e7f48a211ce56d8617bfe`  
		Last Modified: Thu, 21 Nov 2024 23:15:37 GMT  
		Size: 54.5 KB (54532 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:3da04f12c90ba683b1cda93c78d4f8d407e82723d1753b49d3fef1f02dce4f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240842007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef8801a5a2c5059a1e520bd1deb546339d5fcaeb641aa77742a4b74713f0cb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.31
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["php-fpm"]
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa51b96f45aeeeac0da5ce8bef54768006d2f3f15d75cc62bf2f673af4c4ee`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf1193220d0cc95806c6408988e7d5348f9ad83ddfb796cd2261f04ce83160a`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 86.7 MB (86734618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80085106d7b6b1e2208214a2555ef1f1d0e5a1cfb68b48454784f2843f1cdc7e`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b623b8e5969c206320e1845cc6852b92ac54723b937c00e30b8e91c1d60d2a`  
		Last Modified: Tue, 03 Dec 2024 04:41:19 GMT  
		Size: 12.0 MB (12019550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33742b3407425e889a6d0050f76ead7f96951f250671b00188efeadf5461cabc`  
		Last Modified: Tue, 03 Dec 2024 04:41:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1add7bf2fd44e826a9238d12691471b32d27d522eb97913c56aa18675dd2258c`  
		Last Modified: Tue, 03 Dec 2024 04:47:56 GMT  
		Size: 26.1 MB (26099114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bffff2ab679284f7c5711c5dfae40e2b4b36c1a989ab7854b1abba1b61847e8`  
		Last Modified: Tue, 03 Dec 2024 04:47:55 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31498228630d60f9bb080261d2c62659666765b09b6638bdeb8f12dfca1b62f8`  
		Last Modified: Tue, 03 Dec 2024 04:47:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e82ea75f7b25a8beb535fd1c5512369f7f443eb51f9922820cfe415c9c190`  
		Last Modified: Tue, 03 Dec 2024 04:47:55 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5268ab2b1e4cbdc7f5580de536fd6487e7721f0a6b6942a3b7a3b2a41e0221`  
		Last Modified: Tue, 03 Dec 2024 12:29:30 GMT  
		Size: 15.4 MB (15429823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ec3d261fee9cfa63e84769021d82837d8094a0438098bbc1b1649f5098713`  
		Last Modified: Tue, 03 Dec 2024 12:29:30 GMT  
		Size: 970.3 KB (970322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6a2a1bd7e7367201369ee5ea19266a32bde9bda4e76287d6f0f334b01dc72d`  
		Last Modified: Tue, 03 Dec 2024 12:29:30 GMT  
		Size: 16.5 MB (16543967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe521dcc77f4b8affaeedda14a4adc3d877bbcc36806faffcedf033ed9581b67`  
		Last Modified: Tue, 03 Dec 2024 12:29:29 GMT  
		Size: 650.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6616b440467acabd6d2dcd7325bb7831b1e1b219e373cdf7ff912e379032b6ab`  
		Last Modified: Tue, 03 Dec 2024 12:29:32 GMT  
		Size: 54.3 MB (54282395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46429668238d42bed71ed001740806c0338a34719da937c4d9f43f37573ece05`  
		Last Modified: Tue, 03 Dec 2024 12:29:31 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e9cae4e1a6588a031a2ee9f86d92d72c64addb029cf65b3907dbcfbf54c448`  
		Last Modified: Tue, 03 Dec 2024 12:29:31 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:27f57871a49172fe92405d64522e3ce45501dcc640d8cb8de2c27c8beb21ef5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61631acdaf8d30351a655fd40b460bccae63ed664eb68c824bc48ce24779000`

```dockerfile
```

-	Layers:
	-	`sha256:9a8a6d3dde111b29a1e4e15cc200504db09fb88bd52fc7d7992fb5c22779b87e`  
		Last Modified: Tue, 03 Dec 2024 12:29:29 GMT  
		Size: 54.6 KB (54564 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; 386

```console
$ docker pull friendica@sha256:52f6c254e852ab7191a133e2a07eea01cc7c7a07fb17bf744eaddb56de24fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251293006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071af0273c4cff512f63c11719672347ca3561f42b3acc14deec602b5b7e8615`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 19 Aug 2024 01:45:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 Aug 2024 01:45:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_VERSION=8.1.31
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Mon, 19 Aug 2024 01:45:21 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Aug 2024 01:45:21 GMT
WORKDIR /var/www/html
# Mon, 19 Aug 2024 01:45:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 19 Aug 2024 01:45:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 19 Aug 2024 01:45:21 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 19 Aug 2024 01:45:21 GMT
CMD ["php-fpm"]
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35feedeca0a8497bda1fec9c5836e7d00f8e58febae798d87759482317fc91c5`  
		Last Modified: Tue, 03 Dec 2024 02:29:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c016265da121a3f0e46b667a03ebe5e96058997494c11a286c9ead0b6f05d8e`  
		Last Modified: Tue, 03 Dec 2024 02:29:12 GMT  
		Size: 92.5 MB (92521589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f068200f07cb2f7f5d7ac58976b67fb2ba223a19d1eee3bd4bc696f2dcd21e`  
		Last Modified: Tue, 03 Dec 2024 02:29:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3635cba6d9d6a7ce8da73e9e195c800169874951f1dee41405555fea8a199dee`  
		Last Modified: Tue, 03 Dec 2024 02:29:07 GMT  
		Size: 12.0 MB (12019552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77872c2a7586a54793a1e5f1b7c64fc4bceed59266337d082fa859afa202d742`  
		Last Modified: Tue, 03 Dec 2024 02:29:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473e497e985eb0fba2c8cc8aadd540baff3809aac54c41b39ecd2f3df72a0c70`  
		Last Modified: Tue, 03 Dec 2024 02:29:08 GMT  
		Size: 26.5 MB (26536068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad06ba694db513b8c47bc091375d5e529e9c048fa8594bc4667c576bc3e0a898`  
		Last Modified: Tue, 03 Dec 2024 02:29:08 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37c3dd2455440af6a6334cdc559d3774abfe3db239ac1054f05de295e63ab33`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d925944e1f4f4f79f3a34ac4d2d92fed1f0d1bc13e5326919136b086b401bce8`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3cffd62c6130c226ec4786ffc3a63973b1c17a9d9aa5b630fbe76f3c9eaece`  
		Last Modified: Tue, 03 Dec 2024 03:24:13 GMT  
		Size: 16.1 MB (16139074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a7a9a71581a20ab2fba28f7ae395438c44f5e66b48e89f9e72d63e08124273`  
		Last Modified: Tue, 03 Dec 2024 03:24:13 GMT  
		Size: 1.0 MB (1009942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8953aa4c81e81fefd635c0a3308f89fe11a956653acd7f3dbf674df8eab3e3`  
		Last Modified: Tue, 03 Dec 2024 03:24:13 GMT  
		Size: 17.6 MB (17588099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae87937ac642a2f908b01952c4ef0e7361aede97d405a52c29382c06bcdab1d`  
		Last Modified: Tue, 03 Dec 2024 03:24:13 GMT  
		Size: 652.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558b5e46ce00e79b5479861ec2a0d502b1042e60a230dcb6efc08ca5647bac82`  
		Last Modified: Tue, 03 Dec 2024 03:24:15 GMT  
		Size: 54.3 MB (54282310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30238984112526299c137669863058e5d8b39e7c72904d49c81a90188bbb107b`  
		Last Modified: Tue, 03 Dec 2024 03:23:55 GMT  
		Size: 3.2 KB (3182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3770df9b4fa55c2497fc60b9bddab8d0c7688fb4c179cdbd5fcb0ad5a295763`  
		Last Modified: Tue, 03 Dec 2024 03:24:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:a53a29f1127d9ac99a7d6469240c555d21bdb7d56c4eaefc34c554869562f66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 KB (54383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a603679dd3d9aca2e30c35eefe0c671a25d5fb5f6d32e1b5056f2c9897cafe84`

```dockerfile
```

-	Layers:
	-	`sha256:c1ac6fe12248b7ee2d537cceba337b5d294627c00d46c8a738d8b46a1d51c84b`  
		Last Modified: Tue, 03 Dec 2024 03:24:12 GMT  
		Size: 54.4 KB (54383 bytes)  
		MIME: application/vnd.in-toto+json
