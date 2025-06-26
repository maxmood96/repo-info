## `friendica:rc-fpm`

```console
$ docker pull friendica@sha256:fc8456e15e53eb2ea901e90e609aa4efec05642c4ab4ea5cbb839bf0494ece91
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

### `friendica:rc-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:e04351fb797a1698df01de99cc8065213e6c4c4dde4904a5d9e3185692231e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246708708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780765786d3f6f477dd1aa71d1ef56daad928d88c066315c14bb7d55da692c2f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5a5271b8df9c08600af548426538425006d8bf4faf0be5419a4cadca01d4a8`  
		Last Modified: Wed, 25 Jun 2025 19:55:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a384af9670822b984d8bf995d8db9a6402a8dec5eb97ca2030f9d25f132d58`  
		Last Modified: Wed, 25 Jun 2025 19:56:03 GMT  
		Size: 104.3 MB (104331194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120fc30718355661a29b73ac03feb91d7a00563783a41dc98a935031d6d720bb`  
		Last Modified: Wed, 25 Jun 2025 19:55:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d299e353025ab8863ebbe6561f53ba252cc7b5ff0e8eaa12eed2b038acc59`  
		Last Modified: Wed, 25 Jun 2025 19:55:58 GMT  
		Size: 12.7 MB (12664643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6af02ea394997ed51cab8bf8e45253089b14bae44e02b12cef154fc2625817`  
		Last Modified: Wed, 25 Jun 2025 19:55:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d83ff0687cc7f9994e14ddfd67d42f23bd4bfd0eeecfcf05a1e51c9abf9de2a`  
		Last Modified: Wed, 25 Jun 2025 19:55:59 GMT  
		Size: 27.8 MB (27827426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a340e4632546d2875cdcffd97790e056664ada97b4bb8fb68c1ca5756fd5dd33`  
		Last Modified: Wed, 25 Jun 2025 19:55:56 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e13bfe3124eb52618ea62b8dc8f6dbcc2277560807e5b02e4de99ebec41454b`  
		Last Modified: Wed, 25 Jun 2025 19:55:56 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4743670a6d8bba520e89188e88a2f76a6fac1b50776dcabce5ea1bd56f17bc`  
		Last Modified: Wed, 25 Jun 2025 19:55:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447addfc262fba58ebec35a0f755fe06f9c7374f8f3791692b103fa12cc6f775`  
		Last Modified: Wed, 25 Jun 2025 19:55:56 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3400f0009d40481372d9ac4e992c5442c82ae309dc8cb92182574f6a6cbb5f`  
		Last Modified: Thu, 26 Jun 2025 19:05:22 GMT  
		Size: 18.4 MB (18382822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f97a4cf96028b2710e56e4459bcf7ea1ab8fc9290b9e27c2569ccdf46a08eca`  
		Last Modified: Thu, 26 Jun 2025 19:05:21 GMT  
		Size: 1.1 MB (1103692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62415b34892aa1c71b7a84f622782849f3616f0fb3499634d34b0d3f30011a4`  
		Last Modified: Thu, 26 Jun 2025 19:05:26 GMT  
		Size: 35.8 MB (35829573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d50faebecd6c7780145f34122563b083f8e90da75be2c2bbd52367f0ab7727`  
		Last Modified: Thu, 26 Jun 2025 19:05:21 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5545017b91d544cb29bb53d4da10344b3c3d977a55b0c459ad4a8ff76c5fa5d3`  
		Last Modified: Thu, 26 Jun 2025 19:05:21 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3169bc3015cefcbc019c8267bf22b8144a19d177c6a47e66b1cd7d8ca1ec85`  
		Last Modified: Thu, 26 Jun 2025 19:05:21 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306a7774b2a128a074b58787fe723a91f1b80263112ca3057b5fd7527beb4984`  
		Last Modified: Thu, 26 Jun 2025 19:05:24 GMT  
		Size: 18.3 MB (18320087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecff8eb174aef730a5871ed4d7fb3c7c3ad76dd3f3b080d3198169b79c6251`  
		Last Modified: Thu, 26 Jun 2025 19:05:22 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b430dd300f283fe9f8a88dacb54be64aeaa1b0b27a350e34713d8353bb23164`  
		Last Modified: Thu, 26 Jun 2025 19:05:22 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:28bb1b0935ec761ecf556deef256b080a532cc1eea897fec8713614ce2b58310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e503f96569ca9e200da590011d69f3c97dc89cdf71be3236ae5a103fb7ecde`

```dockerfile
```

-	Layers:
	-	`sha256:2755bd5c4e1c7fdad2e4a77b7c3f4dec3ef6c0c1024f92b069228dace6fd3837`  
		Last Modified: Thu, 26 Jun 2025 20:28:54 GMT  
		Size: 59.2 KB (59176 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:6201493e6f14ccdac640f398dab5743c50a7ea52f233c33525dd3f0569411c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217405742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d45b43a9969e6c7c0e32608f78bd2b481f7b49a53917cebc296dbe704ab552`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a4bfa01c4278bce681525640ca665e4be1f8b06675ed34ca66730b92f9f234`  
		Last Modified: Wed, 11 Jun 2025 00:23:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213535e381924aca2ea170c6d78dbba86bf653012096b96d22ac8636c2ac78b1`  
		Last Modified: Wed, 11 Jun 2025 00:23:08 GMT  
		Size: 82.0 MB (81970554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73c797096a39ccf924b52255bfc0ffa99f5d43666673ad5a6492f079a9e1db0`  
		Last Modified: Wed, 11 Jun 2025 00:23:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d485276facd69771e9b945da1351e49087145736cda6baf8ba5ca8e114b36ad5`  
		Last Modified: Wed, 11 Jun 2025 00:50:30 GMT  
		Size: 12.7 MB (12662642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e3a1e87cb17c1f1b76b52c26ce3adf060cf03bb5cfcf8885e2d7051dc774b8`  
		Last Modified: Wed, 11 Jun 2025 00:50:30 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b91ce76e540ef9c77abdab6ad9bb01a0c21310889e5df9413661dcb85ac0d87`  
		Last Modified: Wed, 11 Jun 2025 00:50:31 GMT  
		Size: 26.3 MB (26304977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea57b0857e56ac3ea9776149c2c3a405a43ae59f8814999fcea10de8d2e0a30`  
		Last Modified: Wed, 25 Jun 2025 20:07:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033dd10313f8e4e032596be33a30ac58630b9251843e4f47541092245e667fb`  
		Last Modified: Wed, 25 Jun 2025 20:07:09 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98d04929b5d0ed575c5f327482f14137ba7415220f8e6417b89d146578aa57a`  
		Last Modified: Wed, 25 Jun 2025 20:07:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11116e2ec8bdfaa1d58a22b9fe587b1aee7d3ca615137ad355ddebf6adfc7980`  
		Last Modified: Wed, 25 Jun 2025 20:07:17 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe20f3093b4de7d1199638ecf20c64ac1cace73a3718419af31e5149da3a7bfd`  
		Last Modified: Thu, 26 Jun 2025 19:09:20 GMT  
		Size: 18.1 MB (18103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2b9ec102e8ed3828bb385b9be70bf830a9076e6d2c1d4dfcb38521a126322`  
		Last Modified: Thu, 26 Jun 2025 19:09:19 GMT  
		Size: 1.8 MB (1784327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08c434a5b8e796f9a4bd92d6ad2d40be15ddbd2d32db0b8e0a4546629ba2f9`  
		Last Modified: Thu, 26 Jun 2025 19:09:23 GMT  
		Size: 32.8 MB (32754860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b1afb8fbf61cbaaa7af3987b52cc92c84ffd561533de4996f5645e13af9b62`  
		Last Modified: Thu, 26 Jun 2025 19:09:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1745b4b863cf1dc2d69a16fdec3a13ef8e76e52cc83ea565e6a0907ceb6fef3`  
		Last Modified: Thu, 26 Jun 2025 19:09:19 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2024d3f0e834e0fcd7e1b3be8170ae40c9f3816e948005907365f1faf04f46a7`  
		Last Modified: Thu, 26 Jun 2025 19:09:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3991b8ee243863ac29564d96f1c7ce514675fa67c9030fc9d2ead2822646928f`  
		Last Modified: Thu, 26 Jun 2025 19:09:25 GMT  
		Size: 18.0 MB (18042946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73435423a5b264c4a200a9bbec01dfe2e92191bf9b5ee0d09dabba96dbea67ab`  
		Last Modified: Thu, 26 Jun 2025 19:09:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83138d21ccf3897fc2433f3750639cdf30176b9828824c448b204e25aab75ec6`  
		Last Modified: Thu, 26 Jun 2025 19:09:20 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:c5f7608b6f3e724e297744d7b6015c26f54e8b44eec4892c68729627ff9a3631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec778b08a2c8e4bae85d27f506f7e21267a1b92be12808eb00ec1de7afb847f5`

```dockerfile
```

-	Layers:
	-	`sha256:6447e4f5b093571fbb08f8d8aed80dfaa128bbcd03fc4375b6c4d068d54d146f`  
		Last Modified: Thu, 26 Jun 2025 20:28:57 GMT  
		Size: 59.3 KB (59303 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:39d1ee363b3ece20b989d0ac7aae264c7d75177e43129817bb5070d9f385f907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206777282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537dfb95696f2097cb901d0490a966b68b0ed28d8d896ce74be3c246f8362c90`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7e129ebc47cfb419b9baed6e494c99e8122d50bbdef5c47a23d99fa67bcbb1`  
		Last Modified: Tue, 10 Jun 2025 23:59:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3510790a012b31ddda9feb019968af4c3b5afc39bc69e8a86243793dc1278d31`  
		Last Modified: Wed, 11 Jun 2025 02:02:19 GMT  
		Size: 76.1 MB (76133481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a4467e239356b42185ae523baf135c70abd0641b0d4c23494d1d8a7eaf87c9`  
		Last Modified: Tue, 10 Jun 2025 23:59:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cada066d6ce585c49eb9849297f4e19bec1d14614a9bd1c1b58be1d174a87bc`  
		Last Modified: Wed, 11 Jun 2025 00:45:54 GMT  
		Size: 12.7 MB (12662613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc6facf7f57db59ec1236927cc7cdfcbe022b511f683d023d4c75d624bbe285`  
		Last Modified: Wed, 11 Jun 2025 00:45:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f52eb12cfcfb9a2b6e3cfc9723bcbd573f1e2f190ea734eca7348cf305e138`  
		Last Modified: Wed, 11 Jun 2025 00:45:55 GMT  
		Size: 25.4 MB (25407860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4690e1ca3bb8e26f8c70366020f280be1949e4218690a83003333bad7371e4f`  
		Last Modified: Wed, 25 Jun 2025 19:46:34 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734b6f8d6de3fd8dfd546429eccc0761451da0345bf046c79f28f12fcecf79d`  
		Last Modified: Wed, 25 Jun 2025 19:46:34 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9866959d3b085bd1acd3db6a2fe50670fb055e40c673e0f7e80172d58468654a`  
		Last Modified: Wed, 25 Jun 2025 19:46:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9cc3f719f359fa2bd45e1190db837a4be596aee6a4943e166dc20b67c9fb7f`  
		Last Modified: Wed, 25 Jun 2025 19:46:34 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd1e5caaf9e47c5f51498b2a6de6999f253c2063bfe950a2827edd94872022`  
		Last Modified: Thu, 26 Jun 2025 19:15:38 GMT  
		Size: 18.0 MB (18010209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6763b6623f6894a881137820a2598a766a2ff96f889268eda6a075b440a02f52`  
		Last Modified: Thu, 26 Jun 2025 19:15:36 GMT  
		Size: 1.8 MB (1777467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32155f650762fd6840a7f0522abf681c9eca00bcee02268b8c62c98f512455d`  
		Last Modified: Thu, 26 Jun 2025 19:15:38 GMT  
		Size: 31.0 MB (30951217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36134d825203ce92b392df5e8a47843ed8c0ba6d260308386a0220981f9573d`  
		Last Modified: Thu, 26 Jun 2025 19:15:35 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba2ac833e3946a0a7065502a369469e8a9ff3cbd634024c35e3201eff9be117`  
		Last Modified: Thu, 26 Jun 2025 19:15:36 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2daaf52831e3ed087044a6956dcb097a5d0419d4f40ef44de5a078810d7c66`  
		Last Modified: Thu, 26 Jun 2025 19:15:36 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c134dc71329355b74a38a4e103ce3806b0cd3172ccb1b99253523080248049`  
		Last Modified: Thu, 26 Jun 2025 19:15:39 GMT  
		Size: 17.9 MB (17876527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c42a867cd5d7d301a41c3538562d55ac2976724089f91aab224af9001206029`  
		Last Modified: Thu, 26 Jun 2025 19:15:37 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a83c04176be36f465a2294d8e792e5a5ea302ce9f05e358b89019d4c996ffe`  
		Last Modified: Thu, 26 Jun 2025 19:15:37 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:8178541c7c06639fb1b29bffd29bba3fd6ac7a57825c939275fd4fcd1308087a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6496cc1bba910a28972b93717043ee9a6b5f3f059657fa668de0d38b3b6236`

```dockerfile
```

-	Layers:
	-	`sha256:31fb3202df6fb509dc1cc7e231afd2cf1ad55d307be4cb90ee192ccbe68fc42d`  
		Last Modified: Thu, 26 Jun 2025 20:29:01 GMT  
		Size: 59.3 KB (59303 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:039a2b957f06f2ae4aa1b12cbfbeb731d8ec56bfecf8a670caf988ff49cea7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239120021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e17ae30b7afbe64689dc78eb699f3ede58f05a474454f86a3607ec639d8772`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3630c4a6bfab28c7ce5de97d716ebcd720dbf83dcf0eb1c761482ff53aefecc2`  
		Last Modified: Wed, 11 Jun 2025 00:30:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877a4d3e37c32b0606f0cdd36bf1d42e5e59ac5729fa9e5e94c40a68ebbbd7ff`  
		Last Modified: Wed, 11 Jun 2025 00:31:07 GMT  
		Size: 98.1 MB (98128104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acdc3547850b2843d66bec50193728979d970d5b3dbee391835e42e8af76bd`  
		Last Modified: Wed, 11 Jun 2025 00:30:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cbab49eaae3ca660abf4bdd31a809646d547e7610bdb39102284cfa447cc24`  
		Last Modified: Wed, 11 Jun 2025 00:54:29 GMT  
		Size: 12.7 MB (12664511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5578a297e7fa7dfe136faabb3701636d503d07e8c0c0b8ef9e31528ea50893c`  
		Last Modified: Wed, 11 Jun 2025 00:54:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a3ea348ed4348824c2537879285bf2e214be0e03729d566a0f724496a47f4b`  
		Last Modified: Wed, 11 Jun 2025 01:02:52 GMT  
		Size: 27.8 MB (27800164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38f5c2a182d83192bffff7f2089fe25312295909f684eefe6a01dc66dfc276f`  
		Last Modified: Wed, 25 Jun 2025 20:24:22 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074538d338358f46c8ec1cd28f5082665c9dd8e3f9b2d37954d961e0c28f7072`  
		Last Modified: Wed, 25 Jun 2025 20:24:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dff0c7190de10215c2263e4a4630003e35b6b6f2096873f50e8365d77b0ed5`  
		Last Modified: Wed, 25 Jun 2025 20:24:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd92fcab01040f44ae6968a16bf3887b780e3de8ed48dfbc54f9d15233d70cb4`  
		Last Modified: Wed, 25 Jun 2025 20:24:23 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e5790c16fb25e7d7cde74d0155f6a083c902cccfe5c1c84c9cbf7ec151a900`  
		Last Modified: Thu, 26 Jun 2025 20:29:31 GMT  
		Size: 18.2 MB (18151809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd270cb5f3a8608244e74de743a095cb25245b4f7e06c17fa2ada89994baca0`  
		Last Modified: Thu, 26 Jun 2025 20:04:44 GMT  
		Size: 1.7 MB (1738928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265994bb32a4da560d94e2b8c6afe3cd9d68d888fd911c9f5596acce84a052cb`  
		Last Modified: Thu, 26 Jun 2025 20:29:33 GMT  
		Size: 34.4 MB (34418231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabb48c45d6672781875eb233c60a771fa8016b56efebad1474809491722cd40`  
		Last Modified: Thu, 26 Jun 2025 20:04:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d599f42800bb9ce201b7f6d55b0cb2a184be5acedba6abc8f5af92f68e7ee24`  
		Last Modified: Thu, 26 Jun 2025 20:04:56 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189a77e5243d76ebf6a5a0dce5b1e42255da7f5ed8129f03af9abab36b62f2d8`  
		Last Modified: Thu, 26 Jun 2025 20:04:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f730e21bfc762e4336479cf17f97398708a9ec3b5eea4ca3ba39c17929a23dca`  
		Last Modified: Thu, 26 Jun 2025 20:29:33 GMT  
		Size: 18.1 MB (18121450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61fe3727b37aba9e785707f0c22aa88929f00aa5a48505f79a3e16011bd54bb`  
		Last Modified: Thu, 26 Jun 2025 20:05:03 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3bf0b87913390d1ec684eef5e7b6f4cea767878618ca7f683b9f3c425946a`  
		Last Modified: Thu, 26 Jun 2025 20:05:07 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:c5a060132064329269e0f2f5290f9ff45a0c43ab494055abde94f3882b0b12d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 KB (59336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b538409f630f05489a9699e8dd0691c6f62fcee3d68f26fa3a815375d374dd`

```dockerfile
```

-	Layers:
	-	`sha256:e507492f884e77524284ba3a42a836e6e64700b4b4ed4e242f74801fe58d5a3d`  
		Last Modified: Thu, 26 Jun 2025 20:29:04 GMT  
		Size: 59.3 KB (59336 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; 386

```console
$ docker pull friendica@sha256:b8185d08d9016fe6fb68b3e2b7a359824d90f5d3345e4e6bfacf80dc388b84ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245868009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc34cb9fb2a2236f01365012d3c5b583d68702c9b32959337d04be01dd09f16`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395017dabb1b33af5f93ed9eef8ede718a0200eb6e6d8a65bde638710adfe4e6`  
		Last Modified: Wed, 25 Jun 2025 19:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b10166cd7800056ebf10aeb5dd5afac505652d815ef04f90265a298bc8124a`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 101.5 MB (101515328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fbfdbae16f0f706209ffed76aeb6cd169c99d3303cd536a69152f235c9a2f2`  
		Last Modified: Wed, 25 Jun 2025 19:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f99b3328de0a258431363b1fea31fcffdbd254e9ab7100fdac9a720317485d`  
		Last Modified: Wed, 25 Jun 2025 19:56:27 GMT  
		Size: 12.7 MB (12663730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b961c75a261e466ffebfb2e202da5c39c723d0f6d4acaf5bfab86d01c79be`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568b35ce80aa2126bf710aa3661ed731dde3b56ecac30e518eb7fed2883f7ad8`  
		Last Modified: Wed, 25 Jun 2025 19:56:28 GMT  
		Size: 28.3 MB (28337235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64bbcb93e7a023efe6c4251f3f517aa174d8365bbbec064cfbb34c5331476d`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28361daf87dddf2fd7944f47ea1567fc6d3112315799e1f597ece14064434a5a`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10fe65aa0712bb567af66c71906cc58d7fd446348b9c79aac49b0ce6978d01`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4690c62e2c1ef52a8062711fe807d464912b572743148f0ed7c5a13144df8ec8`  
		Last Modified: Wed, 25 Jun 2025 19:56:25 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb8914dc5b5fb56a2af7b330c7820eb3258e826a2d9144e7b62bc2c0e3b5c26`  
		Last Modified: Thu, 26 Jun 2025 19:05:35 GMT  
		Size: 18.9 MB (18887531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e5becc4939052e5c7fc2f9e2c6bb1fb6e90093684819bc85640754d3282a53`  
		Last Modified: Thu, 26 Jun 2025 19:05:31 GMT  
		Size: 1.1 MB (1078629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bad2ed848798919ccd844e00d0b537924c2c1b6f646bbba50f425d11e45a64b`  
		Last Modified: Thu, 26 Jun 2025 19:05:42 GMT  
		Size: 35.2 MB (35161894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01de3bf01d2951c9c23c99ffcfa2f443641b40c3bb7d8c9bfefcaa8ea3e1c4a`  
		Last Modified: Thu, 26 Jun 2025 19:05:31 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160f02e1dfed4355c9d0e81fd8d1a89750f802ee4173ea7056bd401d945bfcdd`  
		Last Modified: Thu, 26 Jun 2025 19:05:31 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f01c7157546348d4a050f6200555476f397c6ef67f68f9d71c35216ff0c456`  
		Last Modified: Thu, 26 Jun 2025 19:05:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1be53e4366a21f02625d3a1ddd8871bbfea8e6781337f50d692730ba2be2a`  
		Last Modified: Thu, 26 Jun 2025 19:05:35 GMT  
		Size: 19.0 MB (18992102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed169f55f52e1f851c4d3eb5de87937af81589a5712c1aae7e973a8a39b33a6d`  
		Last Modified: Thu, 26 Jun 2025 19:05:32 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b7a9b87c269248735c28575b8ef7fb75b27059700f396ea4521cb0da353e81`  
		Last Modified: Thu, 26 Jun 2025 19:05:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:d8a07aae367e9158c08ea4a1e79e9c1f476ada1fba3277c3b82981073334149a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 KB (59142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43e5c0bac7fd20b1e4782728f84d4064fce6f605dd87d1feb70223b599a34ee`

```dockerfile
```

-	Layers:
	-	`sha256:2e5fd30608b5ceccf73f1ddd754128143e1c05722319dd91fb0608cdca339383`  
		Last Modified: Thu, 26 Jun 2025 20:29:08 GMT  
		Size: 59.1 KB (59142 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:c560d1d6b706d0743bcba21eb1ce1818a0f379ebf7cb82944097c0d8c636f23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219577085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954f23411684a5fd15c0016e3dc3500780aedb78c15095fccb03285c7a3c7e04`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbaad9c575de27a78ec9ecda6c0f021d7843e351bd682abc01e8edfe52f3239`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6a316d668681533c7b3478f23726ec4bacd15c983a623a42fa361b70101e1b`  
		Last Modified: Wed, 11 Jun 2025 01:37:09 GMT  
		Size: 80.7 MB (80670453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cd671d1ab5d1868581d736fae7d6e8644a5d539113a35ec3166149f5fc9c9`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4212d7fefddbcc05d6c8358c4d91e28a3c30e10d2a5dfd2fff6150fe61730ba7`  
		Last Modified: Wed, 11 Jun 2025 05:04:09 GMT  
		Size: 12.7 MB (12662164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745d24827e7bcb5be8a9c249a9904b0a2663563a8a8470d0570fa26db04c85b`  
		Last Modified: Wed, 11 Jun 2025 02:51:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68ab17a83857fd9143fa3999ca86eb8f2c0b1b960e76cda8b7e1fe8ce998d6`  
		Last Modified: Wed, 11 Jun 2025 03:23:13 GMT  
		Size: 26.9 MB (26917016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31715d80e0a3bacbcce8bcb5fb31955713daad52be416cfc87e25ce59789dc7`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d7cb0fa97846ee1c404a5371ba305b4e795358d2db6ef8cf67a34e62c49bd7`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77c7606a1859a7de246c75b0c847e81fad6b8b4360bed40732a6b9acc2afb8f`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ac771756fac3bafedcf21bfefe04160a455c1a7319e09b7eb2465e40a57733`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb72288d20a8817fa289bd0068c2e6f02411b44b5d5c14d26dfc5e6205e4643`  
		Last Modified: Wed, 25 Jun 2025 23:55:27 GMT  
		Size: 17.6 MB (17631517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c642e2462227f36157dff3cdf0b10598e03f7fbf2a33f428d807d1b0b927a408`  
		Last Modified: Wed, 25 Jun 2025 23:55:26 GMT  
		Size: 1.7 MB (1693770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7c151cfaae188e51aa07e23553a39b1e9bae3ce9c4051681f7131d340bf11`  
		Last Modified: Wed, 25 Jun 2025 23:55:29 GMT  
		Size: 33.7 MB (33654312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d96f16151b924d067824a5bdecfa7c7daf0885e199e6ce453811413954087d6`  
		Last Modified: Wed, 25 Jun 2025 23:55:26 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca447a3535f47aa7c3b2accbf10422776def22307fcb036bf09b947170c01a`  
		Last Modified: Wed, 25 Jun 2025 23:55:25 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43b45f798b9ddaad2bcd3f73fd353870781d0f5922e3b3f2c3e246e5a00663a`  
		Last Modified: Wed, 25 Jun 2025 23:55:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df37884799a34488bbd836c775c86b057434e550b7ca20aaa15fd7a797e8d77`  
		Last Modified: Thu, 26 Jun 2025 19:05:16 GMT  
		Size: 17.8 MB (17811975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75be7271e53ecd50e52db782bfef5878b8e60285c4ad1a1351cc5f5809312222`  
		Last Modified: Thu, 26 Jun 2025 19:05:14 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4717e76abab1b3083bc90039940ca4840fc17eaed80523b31f8f77cebd999226`  
		Last Modified: Thu, 26 Jun 2025 19:05:14 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:db6d74b1aee622a14c395da196e63ad0a80b5d64548737705708e2b38efbb7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e68bff053679787ca61a47afeda2dd50f78f13c8ab59554423ed92593f551`

```dockerfile
```

-	Layers:
	-	`sha256:a20f4be29c0557c3cbdfa483f33d853c2102b5541027548b7bfbafdee7658057`  
		Last Modified: Thu, 26 Jun 2025 20:29:11 GMT  
		Size: 59.2 KB (59232 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:2ec65e2556b6de09120241663d0c6f68bed8eb493eafaaf2e71f0fc5558244d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252495941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d520706f0985f7de5c8cb3e2732c2faf1a69969d5f294af28ff8dd39069e07f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24080cf7a9f9030de6956835b567127c780a50d76fe3938c5cd866a6dac26023`  
		Last Modified: Wed, 11 Jun 2025 03:03:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76526385fd8e386cf6c038055e99723ffbb0aa517b93631441caedc0a0753304`  
		Last Modified: Wed, 11 Jun 2025 03:03:51 GMT  
		Size: 103.3 MB (103318539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7e8958d2ce3cdc36201bfc36d3a2d97f4d7a91ae69e3506b18972eee9594fd`  
		Last Modified: Wed, 11 Jun 2025 03:03:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c9dc35678f1cf5155d1f0f16ff62a325defb773116476588733a84c3616a5`  
		Last Modified: Wed, 11 Jun 2025 03:20:30 GMT  
		Size: 12.7 MB (12664127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d15ddcf7aea4f39e8a5cf3e9e8a40fef6bce6dd43243492fc6dd244229b3be9`  
		Last Modified: Wed, 11 Jun 2025 03:20:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7039bd18fa3244226e86638ad4b1c7ccefe4869de5f923387f3da071c1320c0`  
		Last Modified: Wed, 11 Jun 2025 03:28:37 GMT  
		Size: 28.9 MB (28894767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1dd00e7d4097d7a68206e6bf52358cfa703ab7b9e61ed3b77dd6c62e4a153a`  
		Last Modified: Wed, 25 Jun 2025 19:55:48 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e328964ce092c4998fe2e83c4d4d7a687a8aa10f381a4aa0a26a9726c6023776`  
		Last Modified: Wed, 25 Jun 2025 19:55:49 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03eb7166d61adac281322d60833f0507186461c52366442ad9ed99e651c71fb`  
		Last Modified: Wed, 25 Jun 2025 19:55:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8c04504eb8c3b49d2ea74611b99c178904851fa0d9f5968ee600527f5eeaa`  
		Last Modified: Wed, 25 Jun 2025 19:55:49 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b5821277e8705713ae8270a8e6f7f5c85da1583985dd2839f5bc0b6de06d5c`  
		Last Modified: Thu, 26 Jun 2025 19:17:28 GMT  
		Size: 18.5 MB (18464340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c5f70c30c3eaef12b77d18351769503831e500e14a013811cfc8261a562f6`  
		Last Modified: Thu, 26 Jun 2025 19:17:27 GMT  
		Size: 1.7 MB (1727839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3832a1e01c3282d29432bdbc7f0ba7ca30ab49d8314927d20b0356fa225296`  
		Last Modified: Thu, 26 Jun 2025 19:17:31 GMT  
		Size: 36.7 MB (36729400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385aee039eb02c3ca9c0da0a9574e4953d0572bae1a3060e03722ec39d5a91cc`  
		Last Modified: Thu, 26 Jun 2025 19:17:26 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09add35a3249ba7f72bb33f58abf67b31691e30ec9bf61a292df93b9632fb120`  
		Last Modified: Thu, 26 Jun 2025 19:17:26 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1e30182e6c866b9517a26d176815c911bf02f927ab7804508a839f81d312e`  
		Last Modified: Thu, 26 Jun 2025 19:17:26 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94010f3bbc11a2315bad38e8b7e8484a2bf8c6f8e280adcb1a63be64e3201fa0`  
		Last Modified: Thu, 26 Jun 2025 19:17:28 GMT  
		Size: 18.6 MB (18604983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be780430714b2e93ddc675b7fb210f057493228b138a1142ff06040d82cafb0`  
		Last Modified: Thu, 26 Jun 2025 19:17:27 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e03d9d0fda5cba08d92fd29a5ac7a6f4b44020bedd1d5794889153eb64002a`  
		Last Modified: Thu, 26 Jun 2025 19:17:27 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:68ecb7a18f6fd6417d60a54d18d80f4149709fbac53c4d926666ac6a33b2c2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b6760cffe7e2a54cff833427cf99f9a590f44b06a6aff69436f0146117dadc`

```dockerfile
```

-	Layers:
	-	`sha256:5dda07280c426595c01c3da08d244501046e0d42f403dcd8b2f93427db6eab77`  
		Last Modified: Thu, 26 Jun 2025 20:29:15 GMT  
		Size: 59.2 KB (59220 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:5855011ec98c28a22abd995f5b347eb1e389599007a2ae1d9917514613cd41c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216964414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49465d406624f5107ff279a989ea7bed1ffc4ce3fdaf0d4c890c5c45e7d6a2ae`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Jun 2025 09:56:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_VERSION=8.3.22
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Wed, 25 Jun 2025 09:56:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Jun 2025 09:56:45 GMT
WORKDIR /var/www/html
# Wed, 25 Jun 2025 09:56:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Jun 2025 09:56:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Jun 2025 09:56:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Jun 2025 09:56:45 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         msmtp         tini     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	if ! command -v gpg; then 		apt-get install -y --no-install-recommends gnupg2 dirmngr; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         zlib1g-dev         libssl-dev         libgraphicsmagick1-dev         libfreetype6-dev         libwebp-dev         librsvg2-2         libzip-dev         libldap2-dev         libgmp-dev         libmagickcore-6.q16-6-extra     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         exif         zip         opcache         ctype         pcntl         ldap         gmp         intl     ;         pecl install apcu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0 --configureoptions 'enable-redis-zstd="yes" enable-redis-lz4="yes"';     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     fetchDeps="       gnupg     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372fcd6d72a64e9952c1f98b81b9f9773c1b3874422ec0ef84cc9a9401ff8f1`  
		Last Modified: Wed, 11 Jun 2025 00:13:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8ff699d43e5155841feb2101e20cad4c539a873b5f8bc25f50ef7c7ee7597`  
		Last Modified: Wed, 11 Jun 2025 00:13:46 GMT  
		Size: 80.8 MB (80825266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba42c53eb537dcf508d7ad83efac6d9dbe2d8b1f572a7e7de2c5f49afc8a0add`  
		Last Modified: Wed, 11 Jun 2025 00:13:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a8455306e861c7cbafe7488335b1d72bf86d5c4b4a6ddc7aa4115b0042b491`  
		Last Modified: Wed, 11 Jun 2025 00:38:12 GMT  
		Size: 12.7 MB (12663103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439fbc8bd10aba1dba37b60c2d0a463861fadfe6d3b4b76b2f98b09127017652`  
		Last Modified: Wed, 11 Jun 2025 00:38:12 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0534a584f007ed3215814f6de42c08a80bcdd5b31b9e7a736dc91306eff77ec`  
		Last Modified: Wed, 11 Jun 2025 03:36:11 GMT  
		Size: 26.9 MB (26928310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80ca157032a1737a986531ed19fa482ffd29ea5e46f6bebe16ad5a386ce43db`  
		Last Modified: Thu, 26 Jun 2025 00:28:43 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34c0cefe2e33cb5f4c72dbf77e872ae312e84f8de038876637dade05e4bcd89`  
		Last Modified: Thu, 26 Jun 2025 00:28:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c63dfb7ffc53c60e41054a79770c9979bbb1b37f2671f8df787254516e8126`  
		Last Modified: Thu, 26 Jun 2025 00:28:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e10cf6148e7cb1ca804edd646f71f45bb0858423bc6ca018f56afec65aac37`  
		Last Modified: Thu, 26 Jun 2025 00:28:45 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b55bdeb0161e86756228b5aea7f986f89d02bda6dc48f5dc4683480d1a87dc`  
		Last Modified: Thu, 26 Jun 2025 19:12:00 GMT  
		Size: 17.7 MB (17650851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84adc84a0dab8fba885f788a1f7f725bd261a975cde0e5e0c074702ee2d4b91e`  
		Last Modified: Thu, 26 Jun 2025 19:11:58 GMT  
		Size: 1.8 MB (1774754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147ea06174e42ef5a847f93d0324f665a6f1657b7e5d1141be642edb3ce6767e`  
		Last Modified: Thu, 26 Jun 2025 19:12:02 GMT  
		Size: 32.6 MB (32616105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed8b7d97576b896e2834558038894b0325c80ffd26af0ec0d81a5666bf90ca2`  
		Last Modified: Thu, 26 Jun 2025 19:11:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c46ae19d96973927ef2d57f5a1fbd81ded153aecef5d2e0a7785330b02964d5`  
		Last Modified: Thu, 26 Jun 2025 19:12:00 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f095124b93184d4d8738fc8cfb40f45044efdb8cc6961f7abfe61b54e75aeb`  
		Last Modified: Thu, 26 Jun 2025 19:12:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0280d1cbfdae43f7c0a84cc34e005431f9ac1a71f7f64d30b89858475dac2`  
		Last Modified: Thu, 26 Jun 2025 19:12:02 GMT  
		Size: 17.6 MB (17599028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa14c34fce18cc133f3ec121d83dbc170f63655aa28b04f2e1900785285693`  
		Last Modified: Thu, 26 Jun 2025 19:12:01 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13c986bc4b4a2d1674330b6b4d98fdb53ed5bb882f2282de3d45cee75870dc9`  
		Last Modified: Thu, 26 Jun 2025 19:12:01 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm` - unknown; unknown

```console
$ docker pull friendica@sha256:969e47b636734c1dab52bf3162fc76546d2f31cdfc4ae1876cd1e7e34227dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 KB (59166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98e2692ad1515d3af4f47ce942f0bcf0391424a75ba6cd5b3e6130e3e8ddd5`

```dockerfile
```

-	Layers:
	-	`sha256:f3496fb73808a53d745bb7b88a661aaf6682b0c1f2710bca97f1a5b37915d452`  
		Last Modified: Thu, 26 Jun 2025 20:29:18 GMT  
		Size: 59.2 KB (59166 bytes)  
		MIME: application/vnd.in-toto+json
