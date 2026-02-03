## `friendica:stable-fpm`

```console
$ docker pull friendica@sha256:3bff0059407f8895b67bade0f3fd1bc89a5e6b7e5239803b5f118bd9becb1a96
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

### `friendica:stable-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:76a2e32583636fe66d24830a8e448cc193a89967a7aa8591165201a3e719eb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288123969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46231d39447c267ea154d377fd47fc19af5235485c185ee7621b5476531bedfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:23:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:24:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:24:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:24:08 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:34:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:34:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:37:11 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:37:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:37:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:37:11 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:37:11 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 03:32:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:32:16 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:32:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:34:55 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:34:55 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:34:55 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:34:55 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:34:55 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:34:56 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:34:56 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:34:56 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:34:56 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:34:56 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 03:34:56 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 03:34:56 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 03:34:56 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 03:35:12 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:35:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:35:12 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:35:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c87778c77ec62b86d3d20c95f8f31218b822a62477d89a0110eab3c17aa6b`  
		Last Modified: Tue, 03 Feb 2026 02:27:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12e176ed01c5a362872c7a09467e5edbc6009abbf2f9a8b68c4c3edf1ddee7`  
		Last Modified: Tue, 03 Feb 2026 02:27:32 GMT  
		Size: 104.3 MB (104334457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb41d1d279791352b6f2f0446d8b51a36766a6d0643d3b76aa27fef9c2a342b`  
		Last Modified: Tue, 03 Feb 2026 02:27:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe77bc84aef56e2154f4c9d53f464a72c542e1a6bc380ba20286c740cf63d52`  
		Last Modified: Tue, 03 Feb 2026 02:37:23 GMT  
		Size: 12.7 MB (12718696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599ddd230ca96ce6992f486fd0c9e16eee0c150bcf62c1a791ae93b1d797620`  
		Last Modified: Tue, 03 Feb 2026 02:37:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b456fa66d7cc247c5c8b7656f919417ff95d140531544c708d6ddd02c3cdf78`  
		Last Modified: Tue, 03 Feb 2026 02:37:23 GMT  
		Size: 27.8 MB (27845286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb02f8425c9c543f58dc6c3c99c15036d388921d9699b27425d7263a7c90d4ad`  
		Last Modified: Tue, 03 Feb 2026 02:37:22 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14408eee167fc077c4efb4273cc28d89dba1fc9860d893d0f6f2f0cbe44be921`  
		Last Modified: Tue, 03 Feb 2026 02:37:23 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dba5ec52a2eda7df61f05657171d983cda764e47bd60b356d48db6531f7d516`  
		Last Modified: Tue, 03 Feb 2026 02:37:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d65541f3890285afddc05aacf61ceb92f87e5a5cb76221015313b96820fbe36`  
		Last Modified: Tue, 03 Feb 2026 02:37:24 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d67dd5a932e24c8e7e1fb27cd9c6cc6a7a3979e691dbf4b1c040325038c695`  
		Last Modified: Tue, 03 Feb 2026 03:35:22 GMT  
		Size: 18.4 MB (18442032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd60e563cb3bd73b5d01552f57b8781f87eeaefae6fa795caaef0d81c1c94c7`  
		Last Modified: Tue, 03 Feb 2026 03:35:21 GMT  
		Size: 1.1 MB (1104075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069ff7ec79bc9b071a0c898a0e3549ec8988748146ad86e4a7c69e2247ed5d`  
		Last Modified: Tue, 03 Feb 2026 03:35:22 GMT  
		Size: 35.8 MB (35846566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c3a5cdca01f6e2f66c5a99758518abb5b79cb8a8108338a6b9959fdc5a661c`  
		Last Modified: Tue, 03 Feb 2026 03:35:21 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e09baf481257dbea0496ec00dd88585b7ceed68c0e17cd8037fa186332e30e`  
		Last Modified: Tue, 03 Feb 2026 03:35:22 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd7365db8d35765434fae9b262513e5dfd3013d0d346e5e9c4daf0b6d51a2ba`  
		Last Modified: Tue, 03 Feb 2026 03:35:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea2bfde205928be9c7659ef326540e36f5dc3dcc3d2b7469e436c50352432e5`  
		Last Modified: Tue, 03 Feb 2026 03:35:25 GMT  
		Size: 59.6 MB (59585796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eddafcf8ecff2dc0270acc33f7fc0804ab2b464cee5d89302d11f9b73d50f8`  
		Last Modified: Tue, 03 Feb 2026 03:35:23 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864e567b3aa5af7379727d1adafa77f5f1199ac9bd7c1eb6138b5f5d74bb029b`  
		Last Modified: Tue, 03 Feb 2026 03:35:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:66ec2c51062a53eb041f0ef1f8c7fc48f0a0e84a3b084f5d4b823e1ba81acd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e9ac26270873fcb7f3336aa601374c79a17fff8628a1d6a9192be6e0442f9e`

```dockerfile
```

-	Layers:
	-	`sha256:045a7f2777b24d6c6bd78a904944faac219921355051f98657642a52d3ff626a`  
		Last Modified: Tue, 03 Feb 2026 03:35:21 GMT  
		Size: 65.8 KB (65779 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:3ade4e8135e89638c2a10cddb0dd94c1c70fa55724a8870b9b1f25b420d921db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257660422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e33f8097aea844dac0bd298e5ec502745f0859db3fd8689d5f5fb00dd069f12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:21:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:21:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:21:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:21:23 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:46:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:46:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:49:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:49:28 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:49:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:49:28 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:49:28 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:49:28 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 04:45:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 04:45:29 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 04:45:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:48:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:48:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 04:48:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 04:48:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 04:48:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 04:48:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 04:48:39 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 04:48:39 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 04:48:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 04:48:39 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 04:48:39 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 04:48:39 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 04:48:39 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 04:49:01 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:49:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 04:49:01 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 04:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 04:49:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1727b7cfa09c7f6ce5f4a33e26df521f53c82b175ada28fa0086ca9de102a434`  
		Last Modified: Tue, 03 Feb 2026 02:24:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f40817bc2891b3cc60e99cb2af0e4128ddbb3f5091645a9f12e3007af9b52`  
		Last Modified: Tue, 03 Feb 2026 02:24:50 GMT  
		Size: 82.0 MB (81983803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b083ecb053c309c2ccfe9c69b6894d92dff558c98b9a25845d8be513bc1be6`  
		Last Modified: Tue, 03 Feb 2026 02:24:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421a09549d7c94ac260df6246deeab5f41da0a3bfa4aea538bb114c0fecd77fe`  
		Last Modified: Tue, 03 Feb 2026 02:49:39 GMT  
		Size: 12.7 MB (12716563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382eb8c06e2ce6d18ed7019d98abd07d8f896c1a1aa1f58ba9b2d5433389b28`  
		Last Modified: Tue, 03 Feb 2026 02:49:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147e7be7ec1849c843c8c967fa4d31690a712e0b8257df6af7dd94eaffdf3c0`  
		Last Modified: Tue, 03 Feb 2026 02:49:40 GMT  
		Size: 26.3 MB (26303499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ff76f6aa6fc27de7dfcec295b961351d62a1305fddde7e1d2373bfd66d4e91`  
		Last Modified: Tue, 03 Feb 2026 02:49:39 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74365a56ce28d1b52263720b177abcbad136fde12494fd1af42db2b0373dd76c`  
		Last Modified: Tue, 03 Feb 2026 02:49:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34cd9dce45dd1d6491c5ae5480ba16f358703bca4136b430b0256d5cc922cfb`  
		Last Modified: Tue, 03 Feb 2026 02:49:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba56d4a40c07fb1d78802e0f36321f45aa3a2ca3426ec5699572d796814f62e1`  
		Last Modified: Tue, 03 Feb 2026 02:49:41 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5173bc90557079ac9faee1ac2a8d6bb8f36c861040d6516f6ed3f0f41323c0`  
		Last Modified: Tue, 03 Feb 2026 04:49:10 GMT  
		Size: 18.2 MB (18174540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f4249b6f18782db2e8379c8db2f1290936d348a8b2880dad7bcbb118537b7b`  
		Last Modified: Tue, 03 Feb 2026 04:49:10 GMT  
		Size: 1.1 MB (1079419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c5369c12ac1b2e429bb23d24ee26a4c9f842e7da86552e4b97c2252f10d1b`  
		Last Modified: Tue, 03 Feb 2026 04:49:11 GMT  
		Size: 32.0 MB (32043440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c7ce41d80ab7b8e49e2c656feebcb8ed2214d39a8952f4f87d83e6beb04d6c`  
		Last Modified: Tue, 03 Feb 2026 04:49:10 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83423b9c5507524c75ab0f433d4c7549cfc85f7e05d73f3c07283baf4b8808f0`  
		Last Modified: Tue, 03 Feb 2026 04:49:11 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef494507ddfaa0e1e0d16820b2b538cd020106eb430806d152baef1fbcb3f0bb`  
		Last Modified: Tue, 03 Feb 2026 04:49:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b198a5f1d7933930d9867c71edfb32582304904a4173b29f3b0d919dafa91a`  
		Last Modified: Tue, 03 Feb 2026 04:49:13 GMT  
		Size: 59.6 MB (59582961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0a3a4aaedd535cb2ef69dc643b0cd13e40603b4a1633bbcf8db4a285be6fd`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567245c78f83c01771366be09afbe0c4003126e43bd0affd306cf52f2efe9131`  
		Last Modified: Tue, 03 Feb 2026 04:49:12 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:0f1f809a254c0eec75c527244f6d2d77f7810ebfc20f2ecd0d73620c32ddc123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6b2090ee8f48ff3d82ec2bd043a221db40212583479444c952844814eaf9ff`

```dockerfile
```

-	Layers:
	-	`sha256:2a54b9f507a4781f3eb1a8429ec08659be6edb47f2c01fa36225ba4f3027805f`  
		Last Modified: Tue, 03 Feb 2026 04:49:09 GMT  
		Size: 65.9 KB (65918 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:42ffba85d4426dced4f9f7a637fb2725905fe3d31366e367be3bf3cc7501369b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247267232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f5bf72ac33a16d8cbbb821f4028fb8780b72243062154d6e4c97908a98069c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 01:15:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 30 Jan 2026 01:16:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jan 2026 01:16:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jan 2026 01:16:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_VERSION=8.3.30
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 30 Jan 2026 01:16:08 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 30 Jan 2026 01:38:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 30 Jan 2026 01:38:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:41:17 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:41:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:41:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:41:17 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:41:17 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 02:35:06 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:35:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:35:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:38:02 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:38:02 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:38:02 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:38:02 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:38:03 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:38:03 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:38:03 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:38:03 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:38:03 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:38:03 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 30 Jan 2026 02:38:03 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 30 Jan 2026 02:38:03 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 30 Jan 2026 02:38:03 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 30 Jan 2026 02:38:21 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:38:21 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:38:21 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:38:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jan 2026 02:38:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9d718599132958b5a41f75f4ddd3b1f6c53461725982acf8072aafc3b77541`  
		Last Modified: Fri, 30 Jan 2026 01:19:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d62164391405faacd614754a3caa8ec274023544a1b37d231549ccd5cc17beb`  
		Last Modified: Fri, 30 Jan 2026 01:19:24 GMT  
		Size: 76.2 MB (76152516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c838a20b63ccf32725532a92c75f2e3411e0355c159d463086664891cb9592`  
		Last Modified: Fri, 30 Jan 2026 01:19:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32d66f6ea3bb3f293120b35c438b3bcc43b7ba80e6f0710269234b50501670d`  
		Last Modified: Fri, 30 Jan 2026 01:41:29 GMT  
		Size: 12.7 MB (12716545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3974ed29488b3217775144a8237a99b5336868e8b8efbe530b2106314b70f`  
		Last Modified: Fri, 30 Jan 2026 01:41:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926769e14cbed264c2af16dcc1fd7c4e2ab0c87245ff99946ad9eac9f2213c4a`  
		Last Modified: Fri, 30 Jan 2026 01:41:29 GMT  
		Size: 25.4 MB (25409348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af24bc31179424bef1532262e4a398ba568a1ffd112a7bd136fd43237258aa`  
		Last Modified: Fri, 30 Jan 2026 01:41:28 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f0bb6c562f447b277498b33cb2bd57329759373013387bd465cb5dadca15f2`  
		Last Modified: Fri, 30 Jan 2026 01:41:29 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bf24a8d7addb8334358acce1b79ec43a2552b438e5a67a5a65534e80109259`  
		Last Modified: Fri, 30 Jan 2026 01:41:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70663526bba6a5b7444ab5fd55ac83dd50919b700dd5f8104c405d15cdc9151a`  
		Last Modified: Fri, 30 Jan 2026 01:41:31 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f7b588b06e1415437b6ad0b52a369e3487bd180027117ab36a873b3860c545`  
		Last Modified: Fri, 30 Jan 2026 02:38:31 GMT  
		Size: 18.1 MB (18077608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de21f005ea979d0909bfd339a543c3c1efbac1a2beaa9d711bee8a9dc35b4d08`  
		Last Modified: Fri, 30 Jan 2026 02:38:30 GMT  
		Size: 1.1 MB (1070180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adf0840d666dbc7c2cd6a7916c6db98b45df72b71b5122c50c2bef55e2e4324`  
		Last Modified: Fri, 30 Jan 2026 02:38:31 GMT  
		Size: 30.3 MB (30305181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee174beff5094529cf749fa04c558a2b84112649c5487056031478f37381bfc9`  
		Last Modified: Fri, 30 Jan 2026 02:38:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9d2107713046b05cf704792452f40388796d2449c2dd965ba8b0cca8428638`  
		Last Modified: Fri, 30 Jan 2026 02:38:32 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c3cfdccfddb4775049abed6cdde9bd7afb26d8c122cee41296a7823f91e0a`  
		Last Modified: Fri, 30 Jan 2026 02:38:32 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9043a51586c7585048d02b9b6a2b7438ada88ab4cd98734a1c0b6c2ee8ea5cf`  
		Last Modified: Fri, 30 Jan 2026 02:38:34 GMT  
		Size: 59.6 MB (59583180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb903077d01eaaa683eb1189540b226b5db9355e693aba10d6adefdf1fd336c`  
		Last Modified: Fri, 30 Jan 2026 02:38:33 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350aaa7c3f13d74e05c8878e1d72f6c0462eb1000dec32d47246bef86470e92`  
		Last Modified: Fri, 30 Jan 2026 02:38:33 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:9973d52d0b5708418f4be69e97ed26e98417e0c4a98f0ece91fc5cfbc96f91a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 KB (65919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f2bf038f5c46e8676bf209bddc66a6715ab6f4832b201fdd005ee73d9b64c`

```dockerfile
```

-	Layers:
	-	`sha256:2d6855234020d499f9a07f4ba9a0f6c63a623b9f5b440b1135f1c53b829174db`  
		Last Modified: Fri, 30 Jan 2026 02:38:30 GMT  
		Size: 65.9 KB (65919 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:9f47c9b77823a0a00e0fd21eb18d7a63d1a47c6597364305e0433633599df45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279371479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36fab2a8db1ab01130ff7cc6736c7118efb19c69acf103163333a797374074c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:35:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:35:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:35:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:35:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:35:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:35:54 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:36:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:36:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:39:37 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:39:37 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 02:39:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 02:39:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 02:39:37 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 03:50:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:50:56 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:50:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:54:10 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:54:10 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:54:11 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:54:11 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:54:11 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:54:11 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:54:11 GMT
ENV FRIENDICA_VERSION=2024.12
# Tue, 03 Feb 2026 03:54:11 GMT
ENV FRIENDICA_ADDONS=2024.12
# Tue, 03 Feb 2026 03:54:11 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Tue, 03 Feb 2026 03:54:11 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Tue, 03 Feb 2026 03:54:27 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:54:27 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:54:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Feb 2026 03:54:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c3a6e905c54578b26655d3fd313b4356954badbd2c5b465345971e7f37bd4b`  
		Last Modified: Tue, 03 Feb 2026 02:39:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d14abebf6092eb0dd60b4c3cdfd507edd6f7040188871f7081448b57328a71`  
		Last Modified: Tue, 03 Feb 2026 02:40:00 GMT  
		Size: 98.2 MB (98167005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e875bb28bb364d0f23c12a2893f146ac7cf300c408db8f3d37a73462d52dae6c`  
		Last Modified: Tue, 03 Feb 2026 02:39:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f84ad2ac07f83514aca2bd14adc5f9186dbc8a19bc199dc1674b882f38c003`  
		Last Modified: Tue, 03 Feb 2026 02:39:58 GMT  
		Size: 12.7 MB (12718392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a79c80cce6a97baba6afb1adc285f7938a2b3d48e124156389eccc36348122`  
		Last Modified: Tue, 03 Feb 2026 02:39:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e915c0105e9d7b7bb0befb2f75dd260bfe8e48d947a4baf304f7b8161485ae5`  
		Last Modified: Tue, 03 Feb 2026 02:39:59 GMT  
		Size: 27.8 MB (27833683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf0a995bd2fa3effb4424230bc056591bffee91fd5e92da60b28e14235070a4`  
		Last Modified: Tue, 03 Feb 2026 02:39:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1690f7a88010088eb04211fe8b0e9db77082357fae58995a99eca08b0a7d363`  
		Last Modified: Tue, 03 Feb 2026 02:39:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ede5d82c42741b4b4ae6b8992b414a9a1c48ed5d995349d37ff3b3d90cfdb7`  
		Last Modified: Tue, 03 Feb 2026 02:39:49 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd9f6594ed4298c0c8f0cd6aefd4c84d1f062bf22298c4af2026877a6c2ae2`  
		Last Modified: Tue, 03 Feb 2026 02:40:00 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811521f722715ce2d249cbde92270ce589731e38d84365e7686c584769d7d287`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 18.2 MB (18231521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e1fa1918df425577f42bd1815d18a9440aad598461ffcbb81707c6a9c9a8bd`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 1.0 MB (1036178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed0e476e5a60a8446fdee05289047faae1775ab3c21c5465aa40a2e6912f85`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 33.7 MB (33673309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741419c7157be5ab77051433f4410049e8d6118aaab58da71b943153599935d3`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab9fec5342c1d0b16c4338459041d4992043b14823e3ca29887c99a6a826c8e`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193d4022ab90b6fdf153678b218140be819bdce9255f1a9790f2b602f306835f`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698930489fb57487af42c70ad4380b6bca17cc36a598d5a5dab7ed6c8e4f6a`  
		Last Modified: Tue, 03 Feb 2026 03:54:40 GMT  
		Size: 59.6 MB (59584991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3584ef020d25a7881a2539fd5701f787f2c693346497ca9689f8dd4cf647bbf5`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53a6f07e07e9515b3d8cfb84392a4e100ac7225d3a88dbc6f0169037cde17d`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:fafd4c6ca16cebe126fdae0036cf28a46a758b0e0052a27ffae7b5afd0acb666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 KB (65951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ed4c1ebed1ea54007f6fbf337cdd9a229781a498b5b42159e4c750d10ec81`

```dockerfile
```

-	Layers:
	-	`sha256:189f4d8634dc9110c7bb55e3c2a5061d86ce256b93d9cb3c8c9bd3cd9278af0a`  
		Last Modified: Tue, 03 Feb 2026 03:54:36 GMT  
		Size: 66.0 KB (65951 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; 386

```console
$ docker pull friendica@sha256:828b96c99079715fe5f2b4da06495394226dd1813527701fdc75e4eb1abfbf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286604679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d42b1066a6640781981ba3c04c0e928bcbfed049a3d09b013749ac399bca8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 01:18:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 30 Jan 2026 01:18:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jan 2026 01:18:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jan 2026 01:18:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_VERSION=8.3.30
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 30 Jan 2026 01:18:57 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 30 Jan 2026 01:22:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 30 Jan 2026 01:22:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:25:26 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:25:26 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:25:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:25:26 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:25:26 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 02:21:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:21:39 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:21:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:24:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:24:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:24:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:24:22 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:24:23 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:24:23 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:24:23 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:24:23 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:24:23 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:24:23 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 30 Jan 2026 02:24:23 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 30 Jan 2026 02:24:23 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 30 Jan 2026 02:24:23 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 30 Jan 2026 02:24:41 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:24:41 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:24:41 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jan 2026 02:24:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263e9eb321dc1eb3150ebfeb337c8d8d378476e2bd5fd6d5c1790c09ceaf799`  
		Last Modified: Fri, 30 Jan 2026 01:22:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccefd2893e9a2fb3fbed8bb4873c7530d1308dbc432cd338e3050bd3e900cb23`  
		Last Modified: Fri, 30 Jan 2026 01:22:19 GMT  
		Size: 101.5 MB (101524660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d906371ec25417e8cdf38f8369bc0a9254b9755e36b720ba634767336603d2f`  
		Last Modified: Fri, 30 Jan 2026 01:22:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff827b4d85a603258cbe3a22978cfc74b90a13f394ea39deec06977e0a6830e`  
		Last Modified: Fri, 30 Jan 2026 01:25:38 GMT  
		Size: 12.7 MB (12717706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9544b82730718588ef4242d035d2df0f3701c36bc62e33ddd30c259406ec3c`  
		Last Modified: Fri, 30 Jan 2026 01:25:37 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c4f8f13aa91cd61dbe4d486708f05717ee2d569870e32b9fb80cfdf35cee54`  
		Last Modified: Fri, 30 Jan 2026 01:25:38 GMT  
		Size: 28.3 MB (28344701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1b6a2ba297ac7270cd6a6d5eb295e1490807d18ae8f5f9696bbf0044bc6dd`  
		Last Modified: Fri, 30 Jan 2026 01:25:37 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7453ce6e1800a029417a34527d097b6035993491079c213c23adf8e7924d01b`  
		Last Modified: Fri, 30 Jan 2026 01:25:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61992ee094a2df9cc6074683c2ec740892a120b504b39132cd5b9a8ef64ecf9`  
		Last Modified: Fri, 30 Jan 2026 01:25:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e15cf3aafd94c80738dfd0536ff52a56348d21bb6f6812fdfef604e871e772c`  
		Last Modified: Fri, 30 Jan 2026 01:25:39 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672710acd61a9d132a6433166355186597f9119d1caa1e747750c534639732d6`  
		Last Modified: Fri, 30 Jan 2026 02:24:51 GMT  
		Size: 19.0 MB (18963757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04188aefe50488af667f29fd51665b7cbc86d4640dde1a6dfdb28e7c013530e`  
		Last Modified: Fri, 30 Jan 2026 02:24:50 GMT  
		Size: 1.1 MB (1079033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8224a7d54a7595f57f2c45f22dc46f7c95ffdd43096871231d047b44b8572cb6`  
		Last Modified: Fri, 30 Jan 2026 02:24:52 GMT  
		Size: 35.2 MB (35161678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc6c9110d5fc18fbc499e8e0cb1768c5fe0dd43a81bc038c1448438091b4786`  
		Last Modified: Fri, 30 Jan 2026 02:24:50 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e01981fa98005a7a4d5c19c98eede0fa4f313fa787aed2bb96e5b4a3a6bdd3`  
		Last Modified: Fri, 30 Jan 2026 02:24:52 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525851a28a756c6e141c46451c7b3dd3b4a00c185844bec0dc54915e36295ee`  
		Last Modified: Fri, 30 Jan 2026 02:24:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03c048281f93fb9df9f42b7bba816c9906edf03faf3d3fca53fb71e1a9252c4`  
		Last Modified: Fri, 30 Jan 2026 02:24:54 GMT  
		Size: 59.6 MB (59584516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f946f1dc278263098651678d916b0902bd0a52b15924452ec26e563398d0e6`  
		Last Modified: Fri, 30 Jan 2026 02:24:53 GMT  
		Size: 3.2 KB (3158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4906411ec5fd807c5c44131363f8cc2a1ce2c524fe878dfe309374f6e678936`  
		Last Modified: Fri, 30 Jan 2026 02:24:53 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:735734db9be60b56e1c69d70360ba78f856c732a9e096b13da32f900c1ef7c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 KB (65740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7095ec75449d697b1ee4339e3b3667489ba314de061fc242f49c58f5f0c5bdb9`

```dockerfile
```

-	Layers:
	-	`sha256:c9c485ccb00a7bfb04494b805dcd30e0245594903293772b0001cb8b536b825f`  
		Last Modified: Fri, 30 Jan 2026 02:24:50 GMT  
		Size: 65.7 KB (65740 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:39c07138588fce5f18ae2d85b7b0a7900282837106107b1e42fb86baf5284c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262216716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bbe1abd8a62d982f1eadc6d42312bd4b120252f1a8e5286fcee710eb7efc54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:19:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_VERSION=8.3.30
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 13 Jan 2026 01:19:33 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:32:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 17 Jan 2026 00:32:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 01:21:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 01:21:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 01:21:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 01:21:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 01:21:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 01:21:33 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 03:41:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 03:41:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 03:41:42 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 03:41:42 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 04:10:13 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 04:10:59 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 04:10:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 04:23:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 04:23:32 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 04:23:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 04:23:34 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 04:23:35 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 04:23:37 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 04:23:37 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 04:23:37 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 30 Jan 2026 04:24:36 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 04:24:38 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 04:24:39 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 04:24:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jan 2026 04:24:39 GMT
CMD ["php-fpm"]
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
	-	`sha256:8d8602c4056d4c40cee3111cb2dd46373308e77887e6d3a3c59cf5ebb7ff385d`  
		Last Modified: Sat, 17 Jan 2026 00:48:22 GMT  
		Size: 12.7 MB (12716309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4de0bf498f9bb19f02a824d56319e928a03314ec0bf1604bdef5807d8ff015`  
		Last Modified: Sat, 17 Jan 2026 00:48:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba5df0b344522281e8bdfa3d2a3b04e1ad8d57d2aad12fb9fa3594380f0a245`  
		Last Modified: Sat, 17 Jan 2026 01:22:28 GMT  
		Size: 26.9 MB (26937414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ab1e7fde2deafc57bf22c36aaae1f79d3dbef9d2f827b023ac708b4803abf`  
		Last Modified: Sat, 17 Jan 2026 01:22:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36300b062538c90e2d7080fedea8983ac2bc2b9bfcb1a667e1e0a73fb391712`  
		Last Modified: Sat, 17 Jan 2026 01:22:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf699fa9395a6031844210a5f1b6ac838305c4205ac31bf92d1a13e11a148ba`  
		Last Modified: Sat, 17 Jan 2026 01:22:25 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a148d6a3871e963c5e4a34d33f31051a5a930926cdc2090376cced9877623c91`  
		Last Modified: Fri, 30 Jan 2026 03:42:09 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94d71904a5d2e01e4d27f00c5db00879af17513efd5471b995ffd91df3f517a`  
		Last Modified: Fri, 30 Jan 2026 04:25:59 GMT  
		Size: 17.7 MB (17716113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f92839e1f2f3db4dd58c0a09c07317f3f5294081648e2ac933268bec39ced6d`  
		Last Modified: Fri, 30 Jan 2026 04:25:55 GMT  
		Size: 989.6 KB (989616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766feba33afea210a5bed568d18dbd0538740522b63e7d1590b5f2913afb6082`  
		Last Modified: Fri, 30 Jan 2026 04:26:02 GMT  
		Size: 35.1 MB (35067370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4590b618eac6a41826c90a7c58f35a79c75ded24a3d3cee53346732a2fcb35f`  
		Last Modified: Fri, 30 Jan 2026 04:25:55 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f50d8bd7554d4630a3fe9091d47403bdf10b65e3308f8277cc99ed94814aa2a`  
		Last Modified: Fri, 30 Jan 2026 04:25:57 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26714e4fa3937325fffd44d0bf98284b695cff835c481dc77614e9824c0e952`  
		Last Modified: Fri, 30 Jan 2026 04:25:57 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dace051b131ec14e4e8aa20dc9f4976135406defb32793b8f27e1d5482ecad6`  
		Last Modified: Fri, 30 Jan 2026 04:26:07 GMT  
		Size: 59.6 MB (59584495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5b4ec40e8d82c4c66d013a5528f5ed34b268c21a46ce18fb9f434c2689fe7`  
		Last Modified: Sun, 14 Dec 2025 07:14:38 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a6f97343ea2dd92960ffe491e99b5b88caa301999d12e7a4da5caf7471a2ba`  
		Last Modified: Fri, 30 Jan 2026 04:25:59 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:3027419a4a35f030fe5639f1ea9a9d7442a3143c78c337ddfe41819505c94159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5402ef7d3d237440cea0c9626ca0002d7652c3df2c7047db6fea26a2d2217b34`

```dockerfile
```

-	Layers:
	-	`sha256:89eea815cf479b35b2ddc08c3675d85be64717a603921fac2878d7c500c10b56`  
		Last Modified: Fri, 30 Jan 2026 04:25:54 GMT  
		Size: 65.8 KB (65836 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:0c26d613e75c4f0459251661333964b6048e0d85d78309f2b9d7230e33cb8e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294977036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392484adf1d3a147770d12344b7c97901f898d9782a48c09b8f76d49e449052b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

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
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 23:29:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_VERSION=8.3.30
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 13 Jan 2026 23:29:10 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Sat, 17 Jan 2026 00:28:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 17 Jan 2026 00:28:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:41:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 17 Jan 2026 00:41:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:41:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 17 Jan 2026 00:41:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 17 Jan 2026 00:41:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Jan 2026 00:41:29 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 02:17:43 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 02:17:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 02:17:43 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 02:17:43 GMT
CMD ["php-fpm"]
# Fri, 30 Jan 2026 03:42:19 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 03:42:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 03:42:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 03:47:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 03:47:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 03:47:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 03:47:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 03:47:06 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 03:47:06 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 03:47:06 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 03:47:06 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_VERSION=2024.12
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_ADDONS=2024.12
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_DOWNLOAD_SHA256=37bb0fad549c955fced70059b62cd4f3364e344363011a2d054f1b6c425cfb9e
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_DOWNLOAD_ADDONS_SHA256=fbbece635dfaec9d2365581aaafb913cec00128e5815087c9d9b8a46d8dc7ed5
# Fri, 30 Jan 2026 03:56:22 GMT
RUN set -ex;     fetchDeps="         gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 08656443618E6567A39524083EE197EF3F9E4287;         curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz";     curl -fsSL -o friendica-full-${FRIENDICA_VERSION}.tar.gz.asc         "https://files.friendi.ca/friendica-full-${FRIENDICA_VERSION}.tar.gz.asc";     gpg --batch --verify friendica-full-${FRIENDICA_VERSION}.tar.gz.asc friendica-full-${FRIENDICA_VERSION}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_SHA256} *friendica-full-${FRIENDICA_VERSION}.tar.gz" | sha256sum -c;     tar -xzf friendica-full-${FRIENDICA_VERSION}.tar.gz -C /usr/src/;     rm friendica-full-${FRIENDICA_VERSION}.tar.gz friendica-full-${FRIENDICA_VERSION}.tar.gz.asc;     mv -f /usr/src/friendica-full-${FRIENDICA_VERSION}/ /usr/src/friendica;     chmod 777 /usr/src/friendica/view/smarty3;         curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz";     curl -fsSL -o friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc         "https://files.friendi.ca/friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc";     gpg --batch --verify friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc friendica-addons-${FRIENDICA_ADDONS}.tar.gz;     echo "${FRIENDICA_DOWNLOAD_ADDONS_SHA256} *friendica-addons-${FRIENDICA_ADDONS}.tar.gz" | sha256sum -c;     mkdir -p /usr/src/friendica/proxy;     mkdir -p /usr/src/friendica/addon;     tar -xzf friendica-addons-${FRIENDICA_ADDONS}.tar.gz -C /usr/src/friendica/addon --strip-components=1;     rm friendica-addons-${FRIENDICA_ADDONS}.tar.gz friendica-addons-${FRIENDICA_ADDONS}.tar.gz.asc;         gpgconf --kill all;     rm -rf "$GNUPGHOME";         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 03:56:23 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 03:56:24 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 03:56:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jan 2026 03:56:24 GMT
CMD ["php-fpm"]
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
	-	`sha256:0e0b53af54520e190f6a9c40c4d05ac2f403903ce7a8a9e888960a6c3e7a606b`  
		Last Modified: Sat, 17 Jan 2026 00:32:16 GMT  
		Size: 12.7 MB (12718268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c70b3f208bf1e9642d76a585742637b42a7e05b152713ef248b60025caa2ecd`  
		Last Modified: Sat, 17 Jan 2026 00:32:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bf8ba802efef7c483ac9b68ccecd42c7c74d49f3ab4e6d31a15114f1bb0f5e`  
		Last Modified: Sat, 17 Jan 2026 00:42:07 GMT  
		Size: 28.9 MB (28908803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8f4329c4476a2c51232c93fca7898ec343deea36419c2b6945dca9b87fb847`  
		Last Modified: Sat, 17 Jan 2026 00:42:06 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ac865d29ad0b77c311cade8a1b806c387c0433025e14780d1f1dd16d835fab`  
		Last Modified: Sat, 17 Jan 2026 00:42:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356b95fd37b56ee10da9cb1c05ded3d028f3dfab9f738bc22e55df08c78c69ec`  
		Last Modified: Sat, 17 Jan 2026 00:42:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51df64c88010e6115e81458a9bbc5b08feea8f46058a1c2bae27e131c5592c`  
		Last Modified: Fri, 30 Jan 2026 02:18:06 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88fcd03c6d0fa46184f858f19534992b0b906e29d035a6d0007d46d1e57364c`  
		Last Modified: Fri, 30 Jan 2026 03:47:31 GMT  
		Size: 18.6 MB (18558221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bd5d98c89268b5b9f2dd789392648f06f9799b0b27cef119aa3021642078a2`  
		Last Modified: Fri, 30 Jan 2026 03:47:30 GMT  
		Size: 1.0 MB (1026618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e89d24a9353eb36b3f154ab54afe2253fe893d2a4fba7b2c067655ba65dc34`  
		Last Modified: Fri, 30 Jan 2026 03:47:32 GMT  
		Size: 38.8 MB (38762412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff02338e1a6fcf0668653dc920f9a7f3eac0f03073d3191f83d858d2aa90b7`  
		Last Modified: Fri, 30 Jan 2026 03:47:30 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a784df937526d0aeb09739c529d404ed3eb36888c40c8374c58149c4f76e4537`  
		Last Modified: Fri, 30 Jan 2026 03:47:32 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050bdf2d3546fc17e776dd132b247dafbc0fdb6a146d4ab477cfc390a03f8b7`  
		Last Modified: Fri, 30 Jan 2026 03:47:32 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8fbe8f5346c17074dd350a66d8eaa62d3524cbaefb4e26cb25a2a13b95d230`  
		Last Modified: Fri, 30 Jan 2026 03:56:46 GMT  
		Size: 59.6 MB (59586239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acaa133c19549d5e73bac6e9599bb982ecae47fd4fa2807ab0d408953e46462`  
		Last Modified: Fri, 30 Jan 2026 03:56:44 GMT  
		Size: 3.2 KB (3162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31e37d41a96f340050faaa208a35700ad5e94f08b6b0c72ce03c01ffbda1bf6`  
		Last Modified: Fri, 30 Jan 2026 03:56:44 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:b0f7bb0f4e096a128a13e06a3fce8f76129cde2e530693d2bf2ecca5d1f292a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ccac17c7035088cc5bbf6d13601775a4420f412c3b3f14e1c89abc198ba3e0`

```dockerfile
```

-	Layers:
	-	`sha256:afdecbd3a1cadc39de9313243d358ce5c16f6eb0a081dd99a38748083cfe5e24`  
		Last Modified: Fri, 30 Jan 2026 03:56:43 GMT  
		Size: 65.8 KB (65829 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:stable-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:b069dceeaf0a9db524090d99fe100f8525a300dde92e2cb5619aca9b2c1bcd45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257642628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d54de838b99a2a604891a67e5a34008f89e5af8bc3b8a9cc3e052025169274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:29:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:30:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:30:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:30:01 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 03:00:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 03:00:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 03:04:32 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 03:04:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 03 Feb 2026 03:04:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 03 Feb 2026 03:04:32 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 03 Feb 2026 03:04:32 GMT
CMD ["php-fpm"]
# Tue, 03 Feb 2026 05:37:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 05:38:03 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 05:38:03 GMT
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
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
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
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67589198a5f9ec32d48b20c841b986b590309214c0fcdc494b1eb5fc4b9bbf04`  
		Last Modified: Tue, 03 Feb 2026 02:33:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df203e09dcc475ab8aa256ee2f56b9e15c2e42ae8760503a19dc50258f69af4`  
		Last Modified: Tue, 03 Feb 2026 02:33:39 GMT  
		Size: 80.8 MB (80826914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4a27391056de5059325450950dc8d40fb753041ae309ba2b2bc908a5a628d2`  
		Last Modified: Tue, 03 Feb 2026 02:33:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622bd3819c570f55275c0fbea48b0453f06712224729d3d3e238110cb425210`  
		Last Modified: Tue, 03 Feb 2026 03:03:53 GMT  
		Size: 12.7 MB (12716964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0714c0ca117e1aced75ef196c87cdff15b276b9477fe84841b6741763417856f`  
		Last Modified: Tue, 03 Feb 2026 03:03:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c086987674db66ef11bef537699815696def4632f9a99e565a4f08c3eba56b`  
		Last Modified: Tue, 03 Feb 2026 03:04:49 GMT  
		Size: 26.9 MB (26942174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea7439c462d23310a6df0fd1de137d30cc7f76f720743e0c60c9993b33a3c0`  
		Last Modified: Tue, 03 Feb 2026 03:04:49 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b1acb815ec03f08ea469702a278fd13523679a19a0a17cae0d8ef10e01eea4`  
		Last Modified: Tue, 03 Feb 2026 03:04:49 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61de244b166c975b7aa95eec0712e42d89609271cb4b252399a0d274c3d407c`  
		Last Modified: Tue, 03 Feb 2026 03:04:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffd90380532c604302952ff90f1fb3385c7694ed2409ba78bce38add02a30c0`  
		Last Modified: Tue, 03 Feb 2026 03:04:50 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8a9fc6621abb9e667300258af6d2cc9e454a0bbdf62dd6759d8ca3d7b3ef6b`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 17.7 MB (17716689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f13874d4abafabe0f812b5f516ed4e3e13f5597529ecb9c7ebf2a1c35869d45`  
		Last Modified: Tue, 03 Feb 2026 05:40:59 GMT  
		Size: 1.1 MB (1068607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a309e41820b1f961fe90cec425964c32626b484998a901b2a06441f9db182395`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 31.9 MB (31885986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbc82b04675cad6f0794cb89d98c570a8e141f662c8836a0f1bf9d335ed3e78`  
		Last Modified: Tue, 03 Feb 2026 05:40:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719011532806185d1bdda2849430c9cbc873a94e37fdf23a717f63ace02776f0`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154d8dd567b964b3581b0a4cf0b547fc9e40be894b35fa2d47d593fe27095de`  
		Last Modified: Tue, 03 Feb 2026 05:41:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c703e403afc7c3743a06e35b731a5289ea80e1fc5277fa83a2837e3a53b9d2bd`  
		Last Modified: Tue, 03 Feb 2026 05:41:02 GMT  
		Size: 59.6 MB (59582331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3250798d53e98ea8b34e18744ad840117ea190e47fa2206210e71b3ad318fc80`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 3.2 KB (3161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f85c6f9f520510418100440709531cdc2215591a4c346c5f5007b822e8c07b1`  
		Last Modified: Tue, 03 Feb 2026 05:41:01 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:stable-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:f2e8e05aa1e4dd11fcc68ebbd1557bc0a163ffdd5ceb6ab4bb1e89ce4efeed1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 KB (65769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9b6f670824f570670381102ae696a42eeef7afc91cb729085236d79c725b40`

```dockerfile
```

-	Layers:
	-	`sha256:981372b01b6f0879d141fb770a8ea4116afcd45fba4b72ba82e6881ac30769ae`  
		Last Modified: Tue, 03 Feb 2026 05:40:59 GMT  
		Size: 65.8 KB (65769 bytes)  
		MIME: application/vnd.in-toto+json
