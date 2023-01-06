## `phpmyadmin:5-fpm`

```console
$ docker pull phpmyadmin@sha256:2d99202f115252bfe02fdadf521673e1c0e2314956f8f15dac6c9e7cd74ecd80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `phpmyadmin:5-fpm` - linux; amd64

```console
$ docker pull phpmyadmin@sha256:cdc9b3e993338c8d6f219012e583f01a79445c6f7aa7b98fc3ff5cde696b86cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175871948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ef9bb3f5adc713da101a47f76e9e9178c521960bde047964c9556a97d38101`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:54:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:03:13 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:03:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:03:14 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:03:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 01:03:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:12:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:12:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:12:55 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:12:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:12:55 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:12:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:12:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:12:56 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:12:56 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 05:20:28 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:20:28 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 05:20:28 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 05:20:28 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 05:20:29 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 05:20:29 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 05:20:29 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 05:20:29 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 05:20:29 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 05:20:41 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:20:42 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 05:20:42 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 05:20:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:20:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5e2a896f8c67befa1cc14fed28a21d4ab214caba41c3210566609980250081`  
		Last Modified: Fri, 06 Jan 2023 01:54:25 GMT  
		Size: 11.1 MB (11121314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f05b482aafe2bbbc7d418bf4a76b67d6764211993beb833b0393cf86a967a50`  
		Last Modified: Fri, 06 Jan 2023 01:54:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3f2a92cf3ccf60ac0df8cbc15b6f93a1484737a6ed1643b0173096a9b713b`  
		Last Modified: Fri, 06 Jan 2023 01:55:12 GMT  
		Size: 26.0 MB (25968811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badc71de5754cbab1484e57073b4038b96fc24af48ba5a333c47e22250c9f322`  
		Last Modified: Fri, 06 Jan 2023 01:55:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51f886de19b99e0f9e2e40a389d9758a5b2f54a93c9ff97345693bed4e677a1`  
		Last Modified: Fri, 06 Jan 2023 01:55:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786df1c92c3341d1e3169cfd1056c3487943c721b55074316d228ac31fd4fd1f`  
		Last Modified: Fri, 06 Jan 2023 01:55:08 GMT  
		Size: 8.7 KB (8679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf813f70b6141155b5acf1ef60d450dd501a262b6a7a277f74928a884a1e513`  
		Last Modified: Fri, 06 Jan 2023 05:23:04 GMT  
		Size: 3.3 MB (3287409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d2de1f9f5f08879994c54005a00e1e04ec3cb446ac95ee9f74db64c953171`  
		Last Modified: Fri, 06 Jan 2023 05:23:03 GMT  
		Size: 544.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949733c230e6348c7728fa1965d90f746406e497ff78a8118219956194bbfaf0`  
		Last Modified: Fri, 06 Jan 2023 05:23:06 GMT  
		Size: 12.4 MB (12447565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c28afb0e268fd3bcd4e6bb1b29cbaae7a2a808c5b15efe6ef0fd17c141637e`  
		Last Modified: Fri, 06 Jan 2023 05:23:03 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce78030f11327752d846bd327cecee86388456f630913813ad7e124b0615c467`  
		Last Modified: Fri, 06 Jan 2023 05:23:03 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm variant v5

```console
$ docker pull phpmyadmin@sha256:0e721844b3d0972854ab89e60ed0bf358e4427069c904c2c1b87e3e0667b1213
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153442307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d16dfe5f1aff98efde372ca6a7f0e4647895d024f3c79a2dbc638e6af575df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:12:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 03:12:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 03:12:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:12:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 03:12:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 03:12:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:12:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 03:12:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 04:09:51 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 00:34:19 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 00:34:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 00:34:20 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 00:34:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:34:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:51:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:51:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:51:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:51:59 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:52:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:52:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:52:00 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:52:00 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:53:55 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 02:53:55 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 02:53:55 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 02:53:55 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 02:53:55 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 02:53:56 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 02:53:56 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 02:53:56 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 02:53:56 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 02:54:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 02:54:14 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 02:54:14 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 02:54:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 02:54:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9d6b0a4c348f2acc126a26d45600c97234dc9c1280bc45aa1273e17e6a84c1`  
		Last Modified: Wed, 21 Dec 2022 04:29:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c501678603c45e97e3a59b6d68da5b1b8c2c7d722e08be9317819c4261c14897`  
		Last Modified: Wed, 21 Dec 2022 04:29:16 GMT  
		Size: 73.7 MB (73686551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59e0b6e2b0a7211798fe853414b53d3c41263af6fa379898febb3b275ef4856`  
		Last Modified: Wed, 21 Dec 2022 04:29:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e403fa94e1e21826a4597b39cf4dbe65796e5f37e7e82393bca7c1105ced1`  
		Last Modified: Fri, 06 Jan 2023 01:07:03 GMT  
		Size: 11.1 MB (11119554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f2ec7de22a011123caa8f365cd26c4180d4d3c29d2e1b4031fa7d410ed6068`  
		Last Modified: Fri, 06 Jan 2023 01:07:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36664a42e8f500af7c27bbb50717d5a5b1b84cb1149d7f3bd401642969b3317e`  
		Last Modified: Fri, 06 Jan 2023 01:08:10 GMT  
		Size: 24.5 MB (24548424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed9ed38690eddffd428d7bafaf028645961847427388ad7ba1cd8b25b3f7ee5`  
		Last Modified: Fri, 06 Jan 2023 01:08:05 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb82f25b94de90aefab6bd86359ac79e0925a8e3854e244bbeabcd21135dce5`  
		Last Modified: Fri, 06 Jan 2023 01:08:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922f8ee34861aea9ee7e1cb85ff6302572eaaa847d6c15a5a97b8d167bfee89d`  
		Last Modified: Fri, 06 Jan 2023 01:08:05 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75be4a2fa389b5be1cf19221de04348161ee4e234861b9c9d3cd6b56cbe3d151`  
		Last Modified: Fri, 06 Jan 2023 02:55:45 GMT  
		Size: 2.7 MB (2732252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9a59fbb624899a3414101a2b519074e9d9d73a8117c9621dfdf3fd58cc1182`  
		Last Modified: Fri, 06 Jan 2023 02:55:45 GMT  
		Size: 551.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a34898eafa380c59acde48c1b2218b330cd3acede7990abf291ae0f450212a5`  
		Last Modified: Fri, 06 Jan 2023 02:55:48 GMT  
		Size: 12.4 MB (12441726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a050789a161cb38f966b4a4060e0665dbc17130960687fce61403b230b167a`  
		Last Modified: Fri, 06 Jan 2023 02:55:45 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cda9ab541b578a63d6210227157fcfccb015c3a94bc03c1dd56ddf6650e20e`  
		Last Modified: Fri, 06 Jan 2023 02:55:45 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:597dd4bcdff55005464ec6e820bab0ee4bfb7f0ba661cb8888066af4ce7f7881
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145836961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c9592842ba47d00e2ecffc92deab01df0044f7639cb26660dd282b282b28cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 19:49:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 19:49:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 19:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 19:50:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 19:50:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 19:50:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 19:50:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 19:50:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 21:18:49 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 21 Dec 2022 21:18:49 GMT
ENV PHP_VERSION=8.0.26
# Wed, 21 Dec 2022 21:18:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Wed, 21 Dec 2022 21:18:49 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Wed, 21 Dec 2022 21:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 21:19:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 21:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 21:26:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 21:26:32 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 21:26:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 21:26:33 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 21:26:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 21:26:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 21:26:33 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 21:26:34 GMT
CMD ["php-fpm"]
# Thu, 22 Dec 2022 06:02:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 06:02:48 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 22 Dec 2022 06:02:48 GMT
ENV MEMORY_LIMIT=512M
# Thu, 22 Dec 2022 06:02:48 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 22 Dec 2022 06:02:48 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 22 Dec 2022 06:02:49 GMT
ENV VERSION=5.2.0
# Thu, 22 Dec 2022 06:02:49 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Thu, 22 Dec 2022 06:02:49 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Thu, 22 Dec 2022 06:02:49 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 22 Dec 2022 06:03:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 06:03:03 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Thu, 22 Dec 2022 06:03:04 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 22 Dec 2022 06:03:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 22 Dec 2022 06:03:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dbb8de606b0f3d134da534a92e95d7e64924e21a9da63f1acf5f770151b217`  
		Last Modified: Wed, 21 Dec 2022 21:52:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c75b7feafe5c1472546089e973b9927e0deed72e4259fc0d8d21a6a123f927`  
		Last Modified: Wed, 21 Dec 2022 21:52:51 GMT  
		Size: 69.3 MB (69321332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20e1e24e25c1485227c7002e4c00565aa7f85c6c3e4f80b87c5dca435e30f5d`  
		Last Modified: Wed, 21 Dec 2022 21:52:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92d1dc774c4439aec3c1501ad16c819ff3c623050681ddfe433b1cacc8302c6`  
		Last Modified: Wed, 21 Dec 2022 22:07:35 GMT  
		Size: 11.2 MB (11186200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab64e0c33509bf7ddcdb4c815c217470ab13adb58c90856be927002a4b05d5bf`  
		Last Modified: Wed, 21 Dec 2022 22:07:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5304e00b0b2a160e47d413aab82e4ab1b0f8cc752e934ef33c5ce738218955f`  
		Last Modified: Wed, 21 Dec 2022 22:08:35 GMT  
		Size: 23.8 MB (23754263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581ff4d121171923dbe2e35dccc70adfa1e80d27ae2fe124086cab7d9a895139`  
		Last Modified: Wed, 21 Dec 2022 22:08:30 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d671ec2d8591545fb7c15f96f9670e0c1c402d1e3d5866160e938ac4638b0e4d`  
		Last Modified: Wed, 21 Dec 2022 22:08:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48067a98dcfa5f4c3f4bba0c751c2025ae1e592ea287add52b7ae5a66e3b814`  
		Last Modified: Wed, 21 Dec 2022 22:08:30 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6979ed8a2d6dc5ee8dce5eea64b353b2ce8017ab46d4307ceabe638b71b231d2`  
		Last Modified: Thu, 22 Dec 2022 06:04:47 GMT  
		Size: 2.6 MB (2558788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66d6b4a478bf69bc8b63268660d2550dda8e7e33b53c102cc5d69c5b1d74d46`  
		Last Modified: Thu, 22 Dec 2022 06:04:46 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a06397fc95bc0def00d810e9c6528e86ca2fe4db9e078e3b4ea4cccca696bbd`  
		Last Modified: Thu, 22 Dec 2022 06:04:49 GMT  
		Size: 12.4 MB (12441833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef07c1d366960b61019cc407eec38e9ff553574f30eb7237f59c46124516eb60`  
		Last Modified: Thu, 22 Dec 2022 06:04:46 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527e8f5643420b4899e886e7ae9de6d3107b8107fba559761ae83b8b0d3e15ea`  
		Last Modified: Thu, 22 Dec 2022 06:04:46 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:b18d31c7c75e7fa9b628d77761f42c1ceea1ac44840c191a570b3943df0460d0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168866881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb31eed9e0f1ae0d92cfdd19a94653e2c589f27670c4ab7446b10cb35ed379a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 07:44:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:24:32 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:24:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:24:32 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:24:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 01:24:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:31:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:31:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:31:15 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:31:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:31:16 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:31:16 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 05:00:29 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:00:29 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 05:00:29 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 05:00:29 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 05:00:30 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 05:00:30 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 05:00:30 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 05:00:30 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 05:00:30 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 05:00:40 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:00:40 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 05:00:40 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 05:00:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:00:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51709b4373bed589ea5d9f8d001dd50c6d4708cccc0f2b374b7be42d450a0545`  
		Last Modified: Fri, 06 Jan 2023 02:04:22 GMT  
		Size: 11.1 MB (11120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d415b3b0936735ee9db7a77aac059e22ff48c7eeac93e5939f2c96a21460e027`  
		Last Modified: Fri, 06 Jan 2023 02:04:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae13820a91a0715def902dc3edf9b7f595a60089bd6056c7a0c41b5d908b563c`  
		Last Modified: Fri, 06 Jan 2023 02:05:09 GMT  
		Size: 25.4 MB (25394444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1029fa56f17d8c34d116f21dfd0e150d4eb4758ca6f7e263ed48072520b9b7d`  
		Last Modified: Fri, 06 Jan 2023 02:05:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b85c986ab6c51d6b1cf748c4461cad240fed33facb41ff6b5b4963b3de8a31`  
		Last Modified: Fri, 06 Jan 2023 02:05:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2272d831eeb24a945c4f04a5e3d8c36ee85e3552b6dcd60f0919211fa18e3fea`  
		Last Modified: Fri, 06 Jan 2023 02:05:06 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c72dc4c443692886a065c807f4d8bd7ce056dcdb1d0b56a161a72228ae2682`  
		Last Modified: Fri, 06 Jan 2023 05:02:23 GMT  
		Size: 2.9 MB (2920485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7504f413381c8eb67d4b48f237ee59c6f8458b6c96b2049dc0088d55ba1b17c`  
		Last Modified: Fri, 06 Jan 2023 05:02:23 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c96779e1538d0f84a1c18188bb7db615aadfcaa226139eb2d89522725a91a2`  
		Last Modified: Fri, 06 Jan 2023 05:02:25 GMT  
		Size: 12.4 MB (12444799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207bbbee7de794ecd1232d1f7b6d7405797b68891b56b17af8328533a173ff3a`  
		Last Modified: Fri, 06 Jan 2023 05:02:23 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f1bdef4d242b5a47afcb676a857e6eb6c6813d66eff166e79cb90e6ba12bc6`  
		Last Modified: Fri, 06 Jan 2023 05:02:23 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; 386

```console
$ docker pull phpmyadmin@sha256:6ec0592aa8eab49454108adb1f532c076f6eb6c350e7ec2285d1314d3e7cc2c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177612318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629c862754ccc5dbc1af4cd259debf948b0c0dfa9f9c6334b3830bb352b1ecb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:39:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 02:39:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 02:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:39:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 02:39:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 02:39:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:39:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:39:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 04:21:09 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:17:56 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:17:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:17:57 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:18:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 01:18:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:26:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:27:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:27:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:27:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:27:03 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:27:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:27:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:27:06 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:27:07 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 04:57:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 04:57:13 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 04:57:14 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 04:57:15 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 04:57:16 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 04:57:17 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 04:57:18 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 04:57:19 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 04:57:20 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 04:57:34 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 04:57:35 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 04:57:36 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 04:57:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 04:57:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7110976b695f91ec9f6d3d2dba4974dcb6f42afe84906d50adc945fe6584059b`  
		Last Modified: Wed, 21 Dec 2022 04:55:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bad2fa6fb8e9d0bed7870f237359cbb374ecf422d0ec601c64b0c77bd0e059`  
		Last Modified: Wed, 21 Dec 2022 04:55:31 GMT  
		Size: 92.7 MB (92716428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb541bbb0d1d84df303bf8cc14996815ca0ee0de4ca13450a3c4a0a70aba37b`  
		Last Modified: Wed, 21 Dec 2022 04:55:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3588ba98a29d35accac36cf96b6e745cacfd9aa72d17c3d627bd7dde424496`  
		Last Modified: Fri, 06 Jan 2023 02:14:07 GMT  
		Size: 10.9 MB (10904606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b962507f4a43deece1291854aa7e150b68a8867471f09f0f35d9d3f20d2a6a2e`  
		Last Modified: Fri, 06 Jan 2023 02:14:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344bb19ddfd169908dd1bbf3ce12324ccf2720d8427b712ec4fb364f8c3da5a2`  
		Last Modified: Fri, 06 Jan 2023 02:15:04 GMT  
		Size: 26.2 MB (26204682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9db94f8e95de086d06c21f3f3ba2c7bcc08dfc7c40b138b53de48b3c36d3ff2`  
		Last Modified: Fri, 06 Jan 2023 02:15:00 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b3f12c9eb97460db6ac4188af6f3c5f34f342cef9e1c3ae062800d35c875fd`  
		Last Modified: Fri, 06 Jan 2023 02:15:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2310dbdcf37ea594555331b706f481d55df3afba691913584407b678694ce6c1`  
		Last Modified: Fri, 06 Jan 2023 02:15:00 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0115aa2b35a4582b837615b6ff252ae295f51a593166d13eb3a9557268779086`  
		Last Modified: Fri, 06 Jan 2023 05:00:23 GMT  
		Size: 3.2 MB (3167602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b699f4b3b4e75fc64971b79b45aeb32f9f0fe5522849738977c93778eebecf95`  
		Last Modified: Fri, 06 Jan 2023 05:00:23 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd66136b2630bb0d06f4fa1a1cb417f782b661cc5feea4feece2c6e82e0ee8e`  
		Last Modified: Fri, 06 Jan 2023 05:00:26 GMT  
		Size: 12.2 MB (12228061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf63ad81e9a7788e2338eccf06f3ee8e70b34c93be3a670a54b0fd0392422ede`  
		Last Modified: Fri, 06 Jan 2023 05:00:23 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7213da80a47c4aa012cee0bc62d642b544e3dbf6aeb95459e2b86ec158d30902`  
		Last Modified: Fri, 06 Jan 2023 05:00:23 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; mips64le

```console
$ docker pull phpmyadmin@sha256:2e2e357e6305fc8d98b716d6108af8304faeaf0a1ac7253cfb9f2de535a6f915
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152451269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060c94710a5e2468f48d2833b3ae8dca6b8a8da28299f368c06e565a30c38f93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 14:59:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 14:59:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 15:01:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 15:01:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 15:01:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 15:01:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 15:01:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 15:01:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 18:53:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 21 Dec 2022 18:53:50 GMT
ENV PHP_VERSION=8.0.26
# Wed, 21 Dec 2022 18:53:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.26.tar.xz.asc
# Wed, 21 Dec 2022 18:53:58 GMT
ENV PHP_SHA256=0765bfbe640dba37ccc36d2bc7c7b7ba3d2c3381c9cd4305f66eca83e82a40b3
# Wed, 21 Dec 2022 18:54:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 18:54:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:36:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 19:36:21 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 19:36:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 19:36:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 19:36:35 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 19:36:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 19:36:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 19:36:48 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 19:36:52 GMT
CMD ["php-fpm"]
# Thu, 22 Dec 2022 05:30:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 05:30:17 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 22 Dec 2022 05:30:20 GMT
ENV MEMORY_LIMIT=512M
# Thu, 22 Dec 2022 05:30:23 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 22 Dec 2022 05:30:29 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 22 Dec 2022 05:30:33 GMT
ENV VERSION=5.2.0
# Thu, 22 Dec 2022 05:30:36 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Thu, 22 Dec 2022 05:30:39 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Thu, 22 Dec 2022 05:30:43 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 22 Dec 2022 05:31:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 05:31:54 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Thu, 22 Dec 2022 05:31:58 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 22 Dec 2022 05:32:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 22 Dec 2022 05:32:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5a270b32df097d661fbe270a470bd35c56224b48f850e9b1036002daac3603`  
		Last Modified: Wed, 21 Dec 2022 19:51:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4b98b0b273d18374f1846d0509aa5d94de35bdc7c06ac5e4aae4f1f1e37563`  
		Last Modified: Wed, 21 Dec 2022 19:52:20 GMT  
		Size: 72.0 MB (72018901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be37e23167f53c12ded8f61dc0467a44c241de238ea984bb317dac2e030fc1a5`  
		Last Modified: Wed, 21 Dec 2022 19:51:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636068141a74959641b7c7d0961a3724ac4b8b80626aecf8ad4e9c365c761e03`  
		Last Modified: Wed, 21 Dec 2022 20:02:02 GMT  
		Size: 11.0 MB (10969890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eccf769c91d4ecc831e507f6db725d47afad88caa81db60558cf99c7aa7995`  
		Last Modified: Wed, 21 Dec 2022 20:01:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb212668cf4b212f6586b0bc2427280bdb72fa9362b8b64b525b6f39237c1a`  
		Last Modified: Wed, 21 Dec 2022 20:03:24 GMT  
		Size: 25.0 MB (24959538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac600a2b23e11fc5e88b5e2a94246d0af17004159c3c9809811d0844d374dc8`  
		Last Modified: Wed, 21 Dec 2022 20:03:08 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9745d7942622b80a32c67b919bc914c33433196d6d1a8ade6f34fcd53e2ab7`  
		Last Modified: Wed, 21 Dec 2022 20:03:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a3b4dac093f60d95a001e07d12f76d85096c0e62d23c17ea40341db2e60402`  
		Last Modified: Wed, 21 Dec 2022 20:03:08 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100650e973c740703d243654bf88b6454b814c96c7f1883afaca295500dabf7d`  
		Last Modified: Thu, 22 Dec 2022 05:33:15 GMT  
		Size: 2.6 MB (2639064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ad87a513289a159278b4f731f2fcf683b91e267c6533bc27ef8a5bee72a2d3`  
		Last Modified: Thu, 22 Dec 2022 05:33:13 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78659a55e0b34e35552c0619fbfb69282619eac91c6f494372174ad18a440ca`  
		Last Modified: Thu, 22 Dec 2022 05:33:24 GMT  
		Size: 12.2 MB (12228888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c010a1c2397a74e8b9416924355fc170cbc69c5b6fdfabf0f627ca12503578a`  
		Last Modified: Thu, 22 Dec 2022 05:33:13 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f790272a3ff9b90fbaf4f089aceb3dd4fa51073c92d782eda7f4423b773158d9`  
		Last Modified: Thu, 22 Dec 2022 05:33:13 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:61beaf5d375e375ad6d464ddd66bfcddd4ac07ac5c25ca5a4a94868eff2647b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175711780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c40bca7a44a4a56d2cd343c2a6907d00425a00f7de6a832e83a8266e60aff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:54:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 02:54:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 02:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:55:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 02:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 02:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 02:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 04:09:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 00:47:17 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 00:47:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 00:47:18 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 00:47:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:47:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:59:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:59:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:59:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:59:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:59:35 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:59:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:59:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:59:37 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:59:37 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 04:47:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 04:47:52 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 04:47:52 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 04:47:53 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 04:47:54 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 04:47:54 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 04:47:54 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 04:47:55 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 04:47:55 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 04:48:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 04:48:19 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 04:48:20 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 04:48:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 04:48:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7e47853cce58ab3b0e90477d33a7cba4e32fe2c4869183d5b159cc2a331137`  
		Last Modified: Wed, 21 Dec 2022 04:35:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f2925c57c4227f5aaf5bfc813e2b13f014cf5db5bc7ad9f18dd4134fe67a22`  
		Last Modified: Wed, 21 Dec 2022 04:35:43 GMT  
		Size: 86.6 MB (86632961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559957d2a1157e881884b86d6b3ad933922be2896c5787bda3c2c9442a9add8`  
		Last Modified: Wed, 21 Dec 2022 04:35:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d884972c552a55aa120cc501bc56e0c80490a8f02eb2f7b7d6f6ff61d0ac537`  
		Last Modified: Fri, 06 Jan 2023 01:36:12 GMT  
		Size: 11.1 MB (11121177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04af87aadf6f99fec1c049be8e9e34bc725be2afe8cccb26330bd4b79beb82a7`  
		Last Modified: Fri, 06 Jan 2023 01:36:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d919eed317bced0ec634d628b0ca3cc7c509b553d8a3fb34b6a8f1240845116f`  
		Last Modified: Fri, 06 Jan 2023 01:37:21 GMT  
		Size: 27.0 MB (26960268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa49de2d1ec5bc417acdc436ec8a41bbd08d9e99dcd7474ff55bed0a8ef80e9`  
		Last Modified: Fri, 06 Jan 2023 01:37:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ec900ac34afaa76ea59b1d0f69735a4c509e43054f12538f6607bff9465349`  
		Last Modified: Fri, 06 Jan 2023 01:37:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f5d4c0d0f599f27020b17cdc0311a4f7ae48bb3dd5517179f5e249d9fbd9d3`  
		Last Modified: Fri, 06 Jan 2023 01:37:14 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a3aa44d053aa2e650758b1ffebd3f7defe43032d344c6c0832082e714d0697`  
		Last Modified: Fri, 06 Jan 2023 04:51:35 GMT  
		Size: 3.3 MB (3265842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98b9f155c9a6ae3eab0833c8e13dc54b76c21f98ab5086daf93fe33c82aa197`  
		Last Modified: Fri, 06 Jan 2023 04:51:34 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f4d44ce9255c684f7c67fab6bb5cddcd34a4f5997a8fb9cf34c4cb6cabb918`  
		Last Modified: Fri, 06 Jan 2023 04:51:39 GMT  
		Size: 12.4 MB (12447519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b908fdfaa14e7c62f14b2853ac938ef08cf537d92da20a39652e0a3e1cbf883`  
		Last Modified: Fri, 06 Jan 2023 04:51:34 GMT  
		Size: 1.6 KB (1561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc11493437eddd0e2f9c0c83178b6fc5d1f117dff7456e6811bc724d24e3550`  
		Last Modified: Fri, 06 Jan 2023 04:51:34 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:cb7b5de54963a3199e9756db810f86c0531e897f937c1c5df15a28aed905a0be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152756844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff21bcfa899d1743824eb6731cd356eec525c1ecefdfb00f83f75faa23bbb3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 08:46:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 08:46:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 08:47:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 08:47:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 08:47:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 08:47:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 08:47:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 09:48:09 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:15:17 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:15:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:15:18 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:15:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 01:15:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:26:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:26:48 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:26:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:26:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:26:49 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:26:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:26:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:26:51 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:26:51 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 05:09:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:09:22 GMT
ENV MAX_EXECUTION_TIME=600
# Fri, 06 Jan 2023 05:09:22 GMT
ENV MEMORY_LIMIT=512M
# Fri, 06 Jan 2023 05:09:22 GMT
ENV UPLOAD_LIMIT=2048K
# Fri, 06 Jan 2023 05:09:23 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Fri, 06 Jan 2023 05:09:23 GMT
ENV VERSION=5.2.0
# Fri, 06 Jan 2023 05:09:24 GMT
ENV SHA256=66da31ca295f06182ac3f2e6e96057dc824c459baedf4b29de6ed0d3be039230
# Fri, 06 Jan 2023 05:09:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.0/phpMyAdmin-5.2.0-all-languages.tar.xz
# Fri, 06 Jan 2023 05:09:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.0 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Fri, 06 Jan 2023 05:09:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/templates/test/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 05:09:37 GMT
COPY file:dd1a6d4d97f810408e9971c9cb798c969cb1d674fd121696b80d327321562485 in /etc/phpmyadmin/config.inc.php 
# Fri, 06 Jan 2023 05:09:37 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Fri, 06 Jan 2023 05:09:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Jan 2023 05:09:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f06b0a5b87ea33b07c7e0b2ada0ffe18d1394f7d690c637918a2c779b623953`  
		Last Modified: Wed, 21 Dec 2022 10:12:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330fb3f4500910897db299c8d8e47fde1212f6b8d99cf8348ed38274f551d1fa`  
		Last Modified: Wed, 21 Dec 2022 10:12:49 GMT  
		Size: 71.6 MB (71626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a651f7097feb056709f04934684791beade995e9817cdfefdefb820880ecd9b7`  
		Last Modified: Wed, 21 Dec 2022 10:12:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1b0487633db7b1c3b3e680a4a5c48d95a7d90356e809ac842bbbf1f56d22e1`  
		Last Modified: Fri, 06 Jan 2023 01:59:24 GMT  
		Size: 11.1 MB (11120119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c4de4438596b15b8623acdb3ee58cc64c90959f056d70c84f8bf691682358`  
		Last Modified: Fri, 06 Jan 2023 01:59:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac105d42193901ecb4d71aaf5082828d6d89733a596d75ebea1c07209721e45`  
		Last Modified: Fri, 06 Jan 2023 02:00:15 GMT  
		Size: 25.0 MB (25040907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43ce7f6e8a9bd6b976db796efc016a39ffc2ee04f4a79d62a4c7db0dad54830`  
		Last Modified: Fri, 06 Jan 2023 02:00:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1c783cfbe792e851326246bde9642878f05e9f790393c1bb8ffe087e34f28f`  
		Last Modified: Fri, 06 Jan 2023 02:00:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64cb1fe00a4cb320893e83c3310e3ef0624526c0e78d747c042552b91dca286`  
		Last Modified: Fri, 06 Jan 2023 02:00:12 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396ca57e829356898215616e1739f63596caef4e0b1152e1e0596bbb7e288a7d`  
		Last Modified: Fri, 06 Jan 2023 05:11:41 GMT  
		Size: 2.9 MB (2880448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02a2d09a394fcd2ef078fbe0c074f62fdbd0df7e74e8dd13ddf19431a76d39`  
		Last Modified: Fri, 06 Jan 2023 05:11:41 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d7c5c98116c188741c35781df924b86d905b39bb681e9f61109d914cab8923`  
		Last Modified: Fri, 06 Jan 2023 05:11:43 GMT  
		Size: 12.4 MB (12443505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89667fa947cf8767d7aef2c062fd5f2ca8c2ace0c7c5e6552b454eabc081ca6e`  
		Last Modified: Fri, 06 Jan 2023 05:11:41 GMT  
		Size: 1.6 KB (1561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012b6fedba7b78c4f01f679f1c96342ddd6cf556456b05e3672d6c941349a712`  
		Last Modified: Fri, 06 Jan 2023 05:11:41 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
