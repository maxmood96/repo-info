## `friendica:dev-fpm`

```console
$ docker pull friendica@sha256:cb8c27b250e10723e37da80846052e985b6fee2d9156300cd92aa87e2edc05d9
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

### `friendica:dev-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:e2a70ac19cab597267fead592d00f55b2086a25711df76b7d05d812383846f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246909440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734713d83396a801b99d55bfb54b0a447dc19f5850734bcbc4707d665892971d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Tue, 03 Feb 2026 03:32:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:32:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:32:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:34:49 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:34:49 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:34:49 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:34:49 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:34:49 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:34:49 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 03 Feb 2026 03:34:49 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 03 Feb 2026 03:34:53 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 03:34:53 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:34:53 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:34:53 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 03:34:53 GMT
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
	-	`sha256:59d854b64ae73ecc2ad979ca1a42159cfb46482bc3a1b365e8375f39e68e4926`  
		Last Modified: Tue, 03 Feb 2026 03:35:02 GMT  
		Size: 18.4 MB (18442045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6f062fdf05e20b1fcb209e322389a8316bda96e28c6500e8a48111015542d`  
		Last Modified: Tue, 03 Feb 2026 03:35:01 GMT  
		Size: 1.1 MB (1104058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db10ace1f929c3fbdedbd6e5045fc67946202f3271fc8e3b794b1e365d3bc37`  
		Last Modified: Tue, 03 Feb 2026 03:35:02 GMT  
		Size: 35.8 MB (35846374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc777f25acf37f95d96b0069257a9008b6b2c889261509bdb4ec46f70da5bdc`  
		Last Modified: Tue, 03 Feb 2026 03:35:01 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54abe8a39440f85b87f0ab51d7c74ea7e0f4ae26dfc5fe3535c8b400b0a87eb`  
		Last Modified: Tue, 03 Feb 2026 03:35:02 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c048e52d3342427ccbd3a4f4bd13e8be6611a50bd0742a1af166c971db4ba5`  
		Last Modified: Tue, 03 Feb 2026 03:35:02 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6602f07bbf6fdd6a0f4a677d59d0b4ef86f45ceab22066116342f8245365604`  
		Last Modified: Tue, 03 Feb 2026 03:35:03 GMT  
		Size: 18.4 MB (18370765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e7fcfb601e4cc25c0b966fc16294663bef7728307ab28fabefbecbf2b0cd57`  
		Last Modified: Tue, 03 Feb 2026 03:35:03 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3fff98daaee39f669e14ede57753be092f09be5e6fe698f51418e962841fc8`  
		Last Modified: Tue, 03 Feb 2026 03:35:03 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:a0f6db73bca27def66542998763ba27e557604160c3f990d2e54cbc5665c89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab057fefa7a295f6a9bff483f1a12b6c0fc52cb76749bbe6e5d7bca928f0a67`

```dockerfile
```

-	Layers:
	-	`sha256:fffc1c93b28880c19b7a54e5317830ba099ec38033d6b51971f1ef4f8fe623ad`  
		Last Modified: Tue, 03 Feb 2026 03:35:00 GMT  
		Size: 59.1 KB (59146 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:cd8a61bab5df2349c882704057a463b276cf5167e847ffadc522d0c7fab2728c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216171709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1cbd94f361bc7cbebaf3fe9e1f0b38205d6dbf6eaa72f418ed1d44eb77259`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Tue, 03 Feb 2026 04:45:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 04:45:40 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 04:45:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 04:48:45 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:48:45 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 04:48:45 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 04:48:45 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 04:48:45 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 04:48:45 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 04:48:45 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 04:48:45 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 04:48:45 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 04:48:45 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 03 Feb 2026 04:48:45 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 03 Feb 2026 04:48:53 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 04:48:53 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 04:48:53 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 04:48:53 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 04:48:53 GMT
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
	-	`sha256:507c91e729d7f9dd0f84d9639d7aba7419ccf0bbadec61e9d7b1a5d8ae9f0faa`  
		Last Modified: Tue, 03 Feb 2026 04:49:02 GMT  
		Size: 18.2 MB (18174601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df153b3e51984d2779d8c46e83bcae709c56db81ec94f69b0065f00b91516cc`  
		Last Modified: Tue, 03 Feb 2026 04:49:01 GMT  
		Size: 1.1 MB (1079417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3bdbb9c332a06bbdc78ff8d3c99e5acb518c4b429c5a5a3c7975c4cee75dff`  
		Last Modified: Tue, 03 Feb 2026 04:49:02 GMT  
		Size: 32.0 MB (32043372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b514bee06f781c1f4fb9c23b895b9e89f9bcf259e8e9a9c575333073414f0f`  
		Last Modified: Tue, 03 Feb 2026 04:49:01 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9fcc999864c6fee02f9abcff2799765231861f6fe188f9fe72656a2553c6b9`  
		Last Modified: Tue, 03 Feb 2026 04:49:02 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064abb3eb30b027255e3b6f6b351332e380fbe59e3a11f321ee4a6109305a4eb`  
		Last Modified: Tue, 03 Feb 2026 04:49:02 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc8f5ab84b1c89ef72ac1eafcd6a666798b6f4aa41c7c57be3b48b2e71148b`  
		Last Modified: Tue, 03 Feb 2026 04:49:04 GMT  
		Size: 18.1 MB (18093563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9440222d30bf4e6b30731341a30b082e982946f6b8785b74ceef3cfd958712af`  
		Last Modified: Tue, 03 Feb 2026 04:49:03 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0567d5ff79f764c09b88003575db42736861b5340e51e16c8a6fbab714958f0`  
		Last Modified: Tue, 03 Feb 2026 04:49:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:68957419aec15810155ea261459759b0ca38479039109d37fcd978cff06adb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5299e957f7f5041d9ad8d72c522b48587b6d46e76011f04cb5fca7013fad6a95`

```dockerfile
```

-	Layers:
	-	`sha256:4f9fc4563f710afe8df628935e87a4584c6edcd094d5f4796ce627055ac5f543`  
		Last Modified: Tue, 03 Feb 2026 04:49:01 GMT  
		Size: 59.3 KB (59277 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:763d0ab7d1d7e604ed8f5b49f6777eb62c7d273f2552ea95f24c8b11f0cf1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205612541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e40f8887e07709eb22802e362d013d7acc9348d7fe72add3d6c94a57e5e21b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Fri, 30 Jan 2026 02:35:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:35:21 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:35:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:38:00 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:38:00 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:38:00 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:38:00 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:38:00 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:38:00 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:38:00 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:38:00 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:38:00 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:38:00 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 30 Jan 2026 02:38:00 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 30 Jan 2026 02:38:06 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 02:38:06 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:38:06 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:38:06 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 02:38:06 GMT
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
	-	`sha256:9b199a8511d189796749c57ebb7edb058b3cc7629892f51556d6bd37df516bce`  
		Last Modified: Fri, 30 Jan 2026 02:38:13 GMT  
		Size: 18.1 MB (18077613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955f0bd26983d47792ee604bb4b5a1e8e75b1dc9c101f84cc66a7251f0fd64df`  
		Last Modified: Fri, 30 Jan 2026 02:38:13 GMT  
		Size: 1.1 MB (1070156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc32a3970f7a112974596a4df603271891159b20ac72303c60702f246fa9e1b8`  
		Last Modified: Fri, 30 Jan 2026 02:38:14 GMT  
		Size: 30.3 MB (30305153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7290b0aed960e8000b1588ea7193906af6c58ccbb05675dd091f181877c0fa4`  
		Last Modified: Fri, 30 Jan 2026 02:38:13 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cbd771ac4e262bb194b318cfd5fccccfffde227974d344b0fa83fc42715b15`  
		Last Modified: Fri, 30 Jan 2026 02:38:14 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b83031c7d88bbe89f68c01f4d7bdd55d89e6167fe3107cab976c0e04abf3cfe`  
		Last Modified: Fri, 30 Jan 2026 02:38:14 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2309a55fc5ecf0c64ef126792907b4828aca5f21258b06efba1bafc19f98ba5d`  
		Last Modified: Fri, 30 Jan 2026 02:38:15 GMT  
		Size: 17.9 MB (17927844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c67abe49f0720dcc79438c87645cc1ffe7a0b5be21b847a77b97099776f553`  
		Last Modified: Fri, 30 Jan 2026 02:38:15 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd830a4c8b180c4a12a50eca3d899807c8a996b18373dfd770bc156aa484cb3b`  
		Last Modified: Fri, 30 Jan 2026 02:38:15 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:32f997f290dec9dd9bd78812c2b866633fcc51702c2cf807d4965600dd3ed1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4940227db256f9cee875d34b1ff5c8267dfe5338377c696725f7a368a040f0`

```dockerfile
```

-	Layers:
	-	`sha256:ce04df60d1dfe2567154c9263a75ee00b50077d952f978870c0b0bcaad7869ef`  
		Last Modified: Fri, 30 Jan 2026 02:38:12 GMT  
		Size: 59.3 KB (59276 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:dac525b1d468b4834a4c984ef55074e08dea1724693a9a425dd1c827c2173cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (237971957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e25951c327cb9a8e916d067545a8064f8937b4d2af191cb926d6145c1054823`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Tue, 03 Feb 2026 03:51:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 03:51:09 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 03:51:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:54:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:54:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 03:54:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 03:54:25 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 03:54:25 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 03:54:25 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 03:54:25 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 03:54:25 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 03:54:25 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 03:54:25 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 03 Feb 2026 03:54:25 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 03 Feb 2026 03:54:29 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 03:54:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 03:54:29 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 03:54:29 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 03:54:29 GMT
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
	-	`sha256:6a97f2a485ad5ea28f1b357410ecbee7249978d2e3d328d8ca29f5f0d967ae08`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 18.2 MB (18231574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd47d2488b7ae5ad822c4ad97f7b7a9b76bbfcbd3ad960a2bc3d0d546b37393`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 1.0 MB (1036194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec302b971cfedde24bbdda90baad8bccdf2f5981609739e5d678f00df33589c9`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 33.7 MB (33672934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254edf437eddd8689336eda19508efa522cf96d2b640357579ff6e645a3387e4`  
		Last Modified: Tue, 03 Feb 2026 03:54:37 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cd14ae4e5d0e832358b9570062c51fb41394ba339a5716b9d47b5efaf0f2a8`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b0f72679012e438704f1b7dcbde727ca63945c2effceff75411c11e474060e`  
		Last Modified: Tue, 03 Feb 2026 03:54:38 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c80e8006ddebd0399396c5622f6a85e2f24abe1cb14ead45b0f572a2df2add`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 18.2 MB (18185085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c794112677e1a626f2453041841716a8d9091346395a7567905cd646227bed96`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366565420a88171d98688897fe404f96b824968e10762a2a2982764171af7604`  
		Last Modified: Tue, 03 Feb 2026 03:54:39 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:96fe37b47c4b5bcb18d88d233dea43b525daa40dba287e96f407dafc5cd167d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790fcfa9c97ef00231e69e6c11b94584c51fb1f01c0561703512083d6110d3a`

```dockerfile
```

-	Layers:
	-	`sha256:415bb5464cb04d9b007111f33b4a4cb377b0d2f0b28b4c09dfdbdea178c88e23`  
		Last Modified: Tue, 03 Feb 2026 03:54:36 GMT  
		Size: 59.3 KB (59306 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; 386

```console
$ docker pull friendica@sha256:30db8a2810d393052f3ddc707457fb45e1820c3313782be5809df94c331270f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246066777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2edb803e7dbb1a75393f5bd9f62142df64e2955c573a11f78db3d457c897ba`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Fri, 30 Jan 2026 02:21:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Fri, 30 Jan 2026 02:22:01 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 Jan 2026 02:22:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 Jan 2026 02:24:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 02:24:50 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 30 Jan 2026 02:24:50 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 30 Jan 2026 02:24:50 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Fri, 30 Jan 2026 02:24:50 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Fri, 30 Jan 2026 02:24:50 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Fri, 30 Jan 2026 02:24:50 GMT
VOLUME [/var/www/html]
# Fri, 30 Jan 2026 02:24:50 GMT
VOLUME [/var/www/data]
# Fri, 30 Jan 2026 02:24:50 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Fri, 30 Jan 2026 02:24:50 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 30 Jan 2026 02:24:50 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 30 Jan 2026 02:24:55 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 02:24:55 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 02:24:55 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 02:24:55 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 02:24:55 GMT
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
	-	`sha256:aa23741bb3fe40f78e9b4ed56b3ab5e22b488b329778f549f5c6ac0d16156f02`  
		Last Modified: Fri, 30 Jan 2026 02:25:05 GMT  
		Size: 19.0 MB (18963776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25a612825a8ca82126eeb6e0a9fd7ec1ab64a770f74068382b6b5109957430f`  
		Last Modified: Fri, 30 Jan 2026 02:25:04 GMT  
		Size: 1.1 MB (1078982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee7e78282d6a2ef0a05d99d748fc54e97f482224164653dafe6d3c7693e33a3`  
		Last Modified: Fri, 30 Jan 2026 02:25:06 GMT  
		Size: 35.2 MB (35161490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86ce1210bfab1442961d1132c9a903733fe0554f22717508a8e4833e98dbcf`  
		Last Modified: Fri, 30 Jan 2026 02:25:04 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301d1dd416d3a15936da35488585c71f72822a96332fa8b2d592b34190568100`  
		Last Modified: Fri, 30 Jan 2026 02:25:05 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d6a6d0db6ca632818378a7421fc73de4b0000d7a2cc94720f6bcbd5f4cf26`  
		Last Modified: Fri, 30 Jan 2026 02:25:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddcaaa2068773a275540fed7c27dec98c7e9fbc40b965bbd09fa64523bc307d`  
		Last Modified: Fri, 30 Jan 2026 02:25:07 GMT  
		Size: 19.0 MB (19046135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6905e24a77cd6b13b99daad4602bdcfd5aba3bf00c4d03d90c073329ef3d00b1`  
		Last Modified: Fri, 30 Jan 2026 02:25:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781690418acbbd357646e063aaf23d2ad0b1913f94ac7d34d41f65baec588021`  
		Last Modified: Fri, 30 Jan 2026 02:25:07 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:645d0ade2d159ca84c5829a0025c90d667159a8a4dafaac9a1dd1bcb730ab530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86700d98a05716535c599c784e5d82dae4d1002e03120ddd1fc2bc2296310b9d`

```dockerfile
```

-	Layers:
	-	`sha256:3129445159f463041d20539da0b2c1742d4d80c317595492ea8d68ccf1f2f75a`  
		Last Modified: Fri, 30 Jan 2026 02:25:04 GMT  
		Size: 59.1 KB (59112 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:5666cedb0a8a2cf658e097331b38bbd1aff50c72312eddd82516b65095f5c453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220510852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc49c0c5799e16d440916efca095fa863e3f532dfb2f0f33101dcc33ba190ec7`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 30 Jan 2026 04:23:37 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 30 Jan 2026 04:26:55 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 04:26:57 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 04:26:58 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 04:26:58 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 04:26:58 GMT
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
	-	`sha256:00b2e0bdec64afb572a129c240a95875beae6324307c54f1b72acd96c31f4961`  
		Last Modified: Fri, 30 Jan 2026 04:27:45 GMT  
		Size: 17.9 MB (17877942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a15a95e68573864ace996b2d62f34001160fb1664071259df70c888a9b8702`  
		Last Modified: Sat, 17 Jan 2026 02:27:39 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29b41a9e786661d03622b02f242806e8900c69966686f02ec6546c1583334ed`  
		Last Modified: Fri, 30 Jan 2026 04:27:43 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:c4f13ef75689d2801a4dadb7f9e7cc7c021d1a48306148de3e0e8fa1dbfde3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bb18f05e2993aadc59256345f75d6485ba7b81876e21ee3ee3a026ff862229`

```dockerfile
```

-	Layers:
	-	`sha256:5e0632cef062c59da87e8a2da2dc426a8b8b20dad4b6bab88dd2fb24c531f67d`  
		Last Modified: Fri, 30 Jan 2026 04:27:42 GMT  
		Size: 59.2 KB (59194 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:814f01cc8f8f7e1deb47b21dfc50f9571c37a797a21c6f2d6c55fbddcd14be93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254042435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc0201eb20b355eb59f7c8a73a1b8988b34e81c5236799f63a3269d067ba74d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
ENV FRIENDICA_VERSION=2025.02-dev
# Fri, 30 Jan 2026 03:47:06 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Fri, 30 Jan 2026 03:47:15 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Fri, 30 Jan 2026 03:47:15 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 30 Jan 2026 03:47:15 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Fri, 30 Jan 2026 03:47:15 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 30 Jan 2026 03:47:15 GMT
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
	-	`sha256:ecd369b845c62c9d442e670ea3475f96b79bc3ee664ac49e10c71039ee4bdb17`  
		Last Modified: Fri, 30 Jan 2026 03:47:33 GMT  
		Size: 18.7 MB (18650943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff032c436b9f3cdce0df7dc7e932cc111b77451fb110cd4d8811116d56897f9`  
		Last Modified: Fri, 30 Jan 2026 03:47:33 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2029de28e7f42b0bb8eebef14fd3b91c9c395d8a3678413083ff726577efd786`  
		Last Modified: Fri, 30 Jan 2026 03:47:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:7f972521f9f5722b0d5ee91dc8755c68bb990d27a272634386353d4eac3f4d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5441bb7db20915d19f9dc5f38a114532e5bc3258335d89c78da57f66813f6e7e`

```dockerfile
```

-	Layers:
	-	`sha256:febad26776c24614b5704929252c86ce9bb03732da262bba9fc2e8bc9be3d83d`  
		Last Modified: Fri, 30 Jan 2026 03:47:30 GMT  
		Size: 59.2 KB (59189 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:dev-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:c64181cdcb2a76e5a415711e9433174182e61198555c1ef11aaf8b5a8197e6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215708171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6873ed8cbcf556f7ec31988a236cb006a06c0ad07ba5866f0c6081fe4e23d3`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Tue, 03 Feb 2026 05:38:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Tue, 03 Feb 2026 05:38:35 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Feb 2026 05:38:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:40:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.27;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:40:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 03 Feb 2026 05:40:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 03 Feb 2026 05:40:39 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Tue, 03 Feb 2026 05:40:39 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Tue, 03 Feb 2026 05:40:39 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Tue, 03 Feb 2026 05:40:39 GMT
VOLUME [/var/www/html]
# Tue, 03 Feb 2026 05:40:39 GMT
VOLUME [/var/www/data]
# Tue, 03 Feb 2026 05:40:39 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Tue, 03 Feb 2026 05:40:39 GMT
ENV FRIENDICA_VERSION=2025.02-dev
# Tue, 03 Feb 2026 05:40:39 GMT
ENV FRIENDICA_ADDONS=2025.02-dev
# Tue, 03 Feb 2026 05:40:44 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Tue, 03 Feb 2026 05:40:44 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 03 Feb 2026 05:40:44 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Tue, 03 Feb 2026 05:40:44 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 03 Feb 2026 05:40:44 GMT
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
	-	`sha256:8fac9a4315cf5862d54e8acdfb0367746362515560b5e6c4db97ad24420d0ef2`  
		Last Modified: Tue, 03 Feb 2026 05:40:56 GMT  
		Size: 17.7 MB (17716797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb7c9ebf6c93b7276578c3aec4cee3d686fbf70823272cfe9596741fce15fe5`  
		Last Modified: Tue, 03 Feb 2026 05:40:55 GMT  
		Size: 1.1 MB (1068528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc75ff4e19a9d8a0aaebbe9269eb47af6e0b96421fa11e5b7620f587eb0aed4c`  
		Last Modified: Tue, 03 Feb 2026 05:40:56 GMT  
		Size: 31.9 MB (31886044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f7a0491390d840be15be047db98a5066f8a8e9d86160f2a3c27a098c74c8d`  
		Last Modified: Tue, 03 Feb 2026 05:40:55 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffe867414e3e88e1e5923023300f2ec6aa3d75a3f0af2c8a25278b623b9a89d`  
		Last Modified: Tue, 03 Feb 2026 05:40:56 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed20e955f1673eb75d268c3e941992cb8dbcfa6213c151dcecd0f4fe4619351f`  
		Last Modified: Tue, 03 Feb 2026 05:40:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440a512207c1290403a04a3643faaf4fc394e6d051aa4ce8916f2e2b794500c0`  
		Last Modified: Tue, 03 Feb 2026 05:40:57 GMT  
		Size: 17.6 MB (17647089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd017cf19ffd8ef5e7e692b30aed3e6639df377ff79ae984daee8d0b5cbc7da`  
		Last Modified: Tue, 03 Feb 2026 05:40:57 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8991cd6a2ea4eace6dcc9e0139fd983ca6b3d61360fc52c5eee853c63094177b`  
		Last Modified: Tue, 03 Feb 2026 05:40:57 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:dev-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:b5f478f9d707bdb62feeed941831c2163b0ab881020b9d3db2fbaab75831ec86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea4fa3906908e02836f4b25f0a9c806efcfdae7f4654cc460daae38e632262`

```dockerfile
```

-	Layers:
	-	`sha256:7f065a8980931d6e92d64b05699c093fca64b5c7b5ec399d59f156a759490d45`  
		Last Modified: Tue, 03 Feb 2026 05:40:55 GMT  
		Size: 59.1 KB (59136 bytes)  
		MIME: application/vnd.in-toto+json
