## `phpmyadmin:5-fpm`

```console
$ docker pull phpmyadmin@sha256:023a9b40c8e6b3291cee797c6acda7ae738696509dc52c1ad730015a5711aa68
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
$ docker pull phpmyadmin@sha256:ace6e942855a554a0d431a3b21fac050c9466ac57e4806d3e3b527b793dc8919
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189886507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba99103d14205dc33e40cd61164365a4ad802c050a0e246172cc48655c91f8df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:13:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:13:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:13:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:13:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:13:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:13:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 07:14:48 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 07:43:43 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 07:43:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 07:43:43 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 07:43:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 07:43:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:55:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 07:55:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:55:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 07:55:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 07:55:04 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 07:55:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 07:55:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 07:55:05 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 07:55:05 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 19:23:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 19:23:54 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 19:23:54 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 19:23:54 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 19:23:54 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 19:23:54 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 19:23:55 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 19:23:55 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 19:23:55 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 19:23:55 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 19:23:55 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 19:24:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:24:07 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 19:24:07 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 19:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:24:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a95dcec60350663284915f66e96b2d216179ebe405663a818c81de0f22f45e1`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22afa33f327082e95c674a5bdf3b6d25760aca5abce3b032de2c444ba4864ed`  
		Last Modified: Thu, 11 Jan 2024 08:45:06 GMT  
		Size: 104.4 MB (104352766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa61ea11ee8a864fd6b368bd09be18de3692f7ada24f03df32e585107432160`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b26a4eb73f3ef52087ccd57d378c33c229aaeecf88775bf17450e1c3fb84a3`  
		Last Modified: Thu, 11 Jan 2024 08:53:46 GMT  
		Size: 12.4 MB (12394368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9940233e743fed5a8de2a5921125bb212dab75bddb8173b1db1d816ed0638a38`  
		Last Modified: Thu, 11 Jan 2024 08:53:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901a992c080099e8666fa2b6a030d9c6afd5ed67195b04dc8733083cbf6b57e2`  
		Last Modified: Thu, 11 Jan 2024 08:54:31 GMT  
		Size: 27.8 MB (27806723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2641f42d7fac2a20d2c6179018df794f6e09b77c4dbbb07b9afb6ea5d1ee5ce2`  
		Last Modified: Thu, 11 Jan 2024 08:54:28 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b599f2ac4d286bc9f03ef4a379c7bc6ee0c8482350266044ebc0e0cf864ca9`  
		Last Modified: Thu, 11 Jan 2024 08:54:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9965a755a80d517080117b97b6e2425faf6d914e0d807e0e0b213f1cf9c12060`  
		Last Modified: Thu, 11 Jan 2024 08:54:28 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8925afd638386d857cf1f0b5d693f8d19eb5b17aa923c8a609c131e9a3bfd6`  
		Last Modified: Thu, 11 Jan 2024 19:24:56 GMT  
		Size: 3.2 MB (3186938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05fcb92da7cda3c10381c7047d01cef5018444e10eeba70aa22ee9caae8c20`  
		Last Modified: Thu, 11 Jan 2024 19:24:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c4352e7aad18deee4c50a1be851363ef1880ad9921a0b717a9ff4680e17d7c`  
		Last Modified: Thu, 11 Jan 2024 19:24:58 GMT  
		Size: 13.0 MB (13003951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f77141361c1a98e3443331aa4549e2a44f7cac14fab1ed91cf3d5cfcce416d`  
		Last Modified: Thu, 11 Jan 2024 19:24:55 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37594d2c1f77f29437d15f25e50c1b711d2d7dde69a764918abc69245bef01d2`  
		Last Modified: Thu, 11 Jan 2024 19:24:55 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm variant v5

```console
$ docker pull phpmyadmin@sha256:c9dbfb77f83a2f037fb381bfb07afbff1307842ca2ebb0392b75a8784666eb25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163679707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fa826979e32ee50322cae68b556d156d609fc444dcf237b773e31e636e913a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:18:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 02:18:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 02:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:19:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 02:19:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 02:19:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:19:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:19:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 03:07:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 27 Dec 2023 22:47:30 GMT
ENV PHP_VERSION=8.2.14
# Wed, 27 Dec 2023 22:47:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Wed, 27 Dec 2023 22:47:31 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Wed, 27 Dec 2023 22:47:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 22:47:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:10:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 23:10:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:10:55 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 23:10:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 23:10:56 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 23:10:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 27 Dec 2023 23:10:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 27 Dec 2023 23:10:57 GMT
EXPOSE 9000
# Wed, 27 Dec 2023 23:10:58 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 01:53:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 28 Dec 2023 01:53:46 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 28 Dec 2023 01:53:47 GMT
ENV MEMORY_LIMIT=512M
# Thu, 28 Dec 2023 01:53:47 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 28 Dec 2023 01:53:47 GMT
ENV TZ=UTC
# Thu, 28 Dec 2023 01:53:47 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 28 Dec 2023 01:53:48 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 28 Dec 2023 01:53:49 GMT
ENV VERSION=5.2.1
# Thu, 28 Dec 2023 01:53:49 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 28 Dec 2023 01:53:49 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 28 Dec 2023 01:53:49 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 28 Dec 2023 01:54:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 28 Dec 2023 01:54:11 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 28 Dec 2023 01:54:11 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 28 Dec 2023 01:54:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Dec 2023 01:54:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f34b73d2d8e6b1b2c10c6eb4b942988f6ab53d0815dcfbc221d087c716a8b22`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c7dffc50fc2b8f2714576406c9c543112a528c0e55e72bb5dcd48e02d697ba`  
		Last Modified: Tue, 19 Dec 2023 04:48:08 GMT  
		Size: 82.0 MB (81999515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cdf3a474021cac2a6c3b988a5a48cf4a73327b3205a3ba51d644f6035b4456`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bca9d139a6d7e31bee8172ad7805aad2f2ceff3d1223bbb67052f2a3d22c6b8`  
		Last Modified: Thu, 28 Dec 2023 00:34:56 GMT  
		Size: 12.4 MB (12392507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a3d0cf4507f41eddda43b80f1cb1e52633f708db17f2022d8c66fc3ea2cce5`  
		Last Modified: Thu, 28 Dec 2023 00:34:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac3321a5ec637842097cd745b713f9fb8c2da972756667684d6446f6288443`  
		Last Modified: Thu, 28 Dec 2023 00:35:51 GMT  
		Size: 26.8 MB (26782208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f51ed42e285c287f3e5d36c8c5a31692eed06a9c1bff5ece949d6e22d5da2d`  
		Last Modified: Thu, 28 Dec 2023 00:35:45 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08590e4c5d2c5dc366e1c62455e280c856b73fd40b72cbc8635eadd979b9f88e`  
		Last Modified: Thu, 28 Dec 2023 00:35:45 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db5dfdf2be32ba65b801ea45a71f0455bbc43505cdb2f2a3f2ba03f8eb87d57`  
		Last Modified: Thu, 28 Dec 2023 00:35:45 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39159c48c34d9d7ecf833585a1f2749985ab4dd98b06b70dfb1aaea3545fd78d`  
		Last Modified: Thu, 28 Dec 2023 01:55:09 GMT  
		Size: 2.6 MB (2599990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6d4e0eaca5d950417261ed935be87c9fff0474984dc702746ef8bddabcc573`  
		Last Modified: Thu, 28 Dec 2023 01:55:08 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c97596a583bc6c9841414258970bd8e5411af21b5ff39e94cc8e985fe0ecdf7`  
		Last Modified: Thu, 28 Dec 2023 01:55:13 GMT  
		Size: 13.0 MB (13004186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb933221d8a496286873fc6dfbf1bc2e16c4e0d910a22afee7cbeb6ce90bed`  
		Last Modified: Thu, 28 Dec 2023 01:55:08 GMT  
		Size: 1.6 KB (1613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb4fe21d0593ce1ff97e1e36da1ad80d49a7cf42b79a586e28228d7a086cf0e`  
		Last Modified: Thu, 28 Dec 2023 01:55:08 GMT  
		Size: 781.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm variant v7

```console
$ docker pull phpmyadmin@sha256:b31a59f34d224b61c43ce99e62834942ef5b7f1f71f285149ac8667e080ba0a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154150733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4739d2618d0fe55f391e81a8054cdeadbfe285394b932b0b0b507684616f435`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:01:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 07:01:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 07:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:01:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 07:01:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 07:01:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 07:01:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 07:01:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 08:32:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 09:25:43 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 09:25:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 09:25:43 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 09:26:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 09:26:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:46:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 09:46:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 09:46:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 09:46:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 09:46:25 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 09:46:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 09:46:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 09:46:28 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 09:46:28 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 23:25:00 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 23:25:00 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 23:25:00 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 23:25:01 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 23:25:01 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 23:25:01 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 23:25:03 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 23:25:03 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 23:25:04 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 23:25:04 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 23:25:04 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 23:25:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 23:25:23 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 23:25:23 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 23:25:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 23:25:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78480f120d1bf6d4d635fb5b3b6c319e732dd057429d1179f5e8a7c8435599bf`  
		Last Modified: Thu, 11 Jan 2024 11:11:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b281e927e3ce40bca6838ab4b25427cc76d3bc1fe6d5d47703c2197862df8`  
		Last Modified: Thu, 11 Jan 2024 11:12:06 GMT  
		Size: 76.2 MB (76167092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b9c5e142ab0229e1d7a3ed2041f80a73142bf9108777851a45069945807a61`  
		Last Modified: Thu, 11 Jan 2024 11:11:47 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd24e197efcdad29d2f216bc42dedd81b50debf85f70e974506127e7d2d5a709`  
		Last Modified: Thu, 11 Jan 2024 11:21:51 GMT  
		Size: 12.4 MB (12392561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8247b1c2ce24da475b4ed1980eb4dcfeac5ea74e9d9b0de1f7328a96416831c`  
		Last Modified: Thu, 11 Jan 2024 11:21:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c155809aa3da6216181f795269cdc20f9c335a376a0c9c8c7b0ca945616b2d`  
		Last Modified: Thu, 11 Jan 2024 11:22:42 GMT  
		Size: 25.4 MB (25412732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71da2548c547c00a8f3f3c07cce2b32521fd94c2f756b1a3f93c8d30226858`  
		Last Modified: Thu, 11 Jan 2024 11:22:37 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a322d16b06ec9357457cbf27d023ab6480a366508d7642f5670c41964af9275e`  
		Last Modified: Thu, 11 Jan 2024 11:22:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c40011f6c7fd879d418ed449ac86ad4a606944ea6ee82d0c67f53e0d0e7700b`  
		Last Modified: Thu, 11 Jan 2024 11:22:37 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae22393a965125f2c7963b184beba8f283279416c9132754f21d30d196b92cc5`  
		Last Modified: Thu, 11 Jan 2024 23:26:30 GMT  
		Size: 2.4 MB (2440105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1696acab798a72ddd2d59d11624078ba00bf060ee5a8ee4578cc1c2c0e7f1b78`  
		Last Modified: Thu, 11 Jan 2024 23:26:29 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee72eb0acb441210b14f2430973a2c54fa176ed99dcecd4f2a06fc83203d90f`  
		Last Modified: Thu, 11 Jan 2024 23:26:33 GMT  
		Size: 13.0 MB (13004275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0031b3a346002101037df65fb9380a1010b867d8aa4d3633780c4560cbe52f35`  
		Last Modified: Thu, 11 Jan 2024 23:26:29 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e097534075100a43e7c2d2a94a4b507ced11b0695aace32bb2377b55dbcc7774`  
		Last Modified: Thu, 11 Jan 2024 23:26:29 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; arm64 variant v8

```console
$ docker pull phpmyadmin@sha256:f894090a1216b746328999bfb3f23510ad40f84ecca19f5739918e9180fc2300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183905820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6076537b63a896dc002cd2561e35433661a3fb1bcc30d2080b9505c080d45be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 03:30:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 03:30:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 03:30:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 03:30:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 03:30:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 03:30:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 04:26:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 04:51:53 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 04:51:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 04:51:53 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 04:52:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 04:52:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:02:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 05:02:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:02:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 05:02:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 05:02:02 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 05:02:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 05:02:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 05:02:03 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 05:02:03 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 10:39:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 10:39:23 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 10:39:23 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 10:39:23 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 10:39:23 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 10:39:23 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 10:39:23 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 10:39:24 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 10:39:24 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 10:39:24 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 10:39:24 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 10:39:33 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 10:39:33 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 10:39:33 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 10:39:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 10:39:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451161081bb50dfa3757568668f099cf58479733644abdbc5c2f79d7c4d9cade`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e283d29837ef0a320a5446924b58fe28a48bdb544e3b65cc753b44483e58aa4`  
		Last Modified: Thu, 11 Jan 2024 05:46:13 GMT  
		Size: 98.1 MB (98128972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99cfb51d5dc36e05dbed790e970497125214a08a60c68ef185661b1a6638e4a`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd94d2c241fdde5c426494d278e3a2fa06f36a9c91e0c97059fe6622c07af2f3`  
		Last Modified: Thu, 11 Jan 2024 05:54:28 GMT  
		Size: 12.4 MB (12394253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90ce3ebbaf8a25ba9da00ed2c0c169e24b952593a06b1e8347f12a6ed4963d1`  
		Last Modified: Thu, 11 Jan 2024 05:54:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a615285100daa89d8ca728ec7decbcf43f9db7ae7ee6a323a94a2e65d40a8849`  
		Last Modified: Thu, 11 Jan 2024 05:55:12 GMT  
		Size: 27.8 MB (27768576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26e259c23c65e8ef4c1260ecf63e4bd12f0318f95e85df64ccc37fb5d0fba0d`  
		Last Modified: Thu, 11 Jan 2024 05:55:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee16e46060e0852e63df0fad66a8041851e7e745b7a5c7e521aa74927b7e03a8`  
		Last Modified: Thu, 11 Jan 2024 05:55:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3df4c82303e7f0c43650feae05c85db176b4ac35d0a34965e14dbb0097b45d`  
		Last Modified: Thu, 11 Jan 2024 05:55:09 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701b2dcb72713cebda1ea12ad02db769c30d8d24d93f4f89d966427d1f9ecaed`  
		Last Modified: Thu, 11 Jan 2024 10:40:28 GMT  
		Size: 3.4 MB (3436721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83114cae1862086284cd60ffbfbe3089d7f41cf4e2bd8cc47fc0b0cb89ebe5f1`  
		Last Modified: Thu, 11 Jan 2024 10:40:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d796bc9207347f1fd6b2cb07275d36ac0990eaceb061eef1ea91af1154d4baa`  
		Last Modified: Thu, 11 Jan 2024 10:40:29 GMT  
		Size: 13.0 MB (13004112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdc77a7c5342e20220bcca40be0a61eadcb1e3cd5ee3c8009df2d92ad0822eb`  
		Last Modified: Thu, 11 Jan 2024 10:40:27 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a47b66eee57b3e716e2a3df682b69fe00ccf76cb149ab8fcb0cf7ee0a00d43`  
		Last Modified: Thu, 11 Jan 2024 10:40:27 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; 386

```console
$ docker pull phpmyadmin@sha256:2398a6f2577552e18bc36891e32bb637f3a375eedd9c24667d3d0e67e124229c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188694926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0152b4afecd002c81bbc7773de8d6d7e2b52c2b457c3e95d9795e434492f3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:58:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 04:58:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 04:58:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:58:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 04:58:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 04:58:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:58:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:58:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 06:40:02 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 07:29:02 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 07:29:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 07:29:02 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 07:29:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 07:29:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:49:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 07:49:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:49:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 07:49:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 07:49:09 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 07:49:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 07:49:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 07:49:09 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 07:49:09 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 19:12:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 19:12:33 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 19:12:33 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 19:12:33 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 19:12:33 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 19:12:33 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 19:12:34 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 19:12:34 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 19:12:34 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 19:12:34 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 19:12:34 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 19:12:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:12:51 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 19:12:51 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 19:12:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 19:12:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946df82896e7966597c6491529e0230dd6f4ba0b305c589840bc9133f0535fa4`  
		Last Modified: Thu, 11 Jan 2024 09:11:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d33e770c7aaf9e80071255e0e21cfc96139d4398eeda332ed50d769a3e6b0`  
		Last Modified: Thu, 11 Jan 2024 09:11:46 GMT  
		Size: 101.5 MB (101534598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97c877b297ab5b95038cd30ec523bacef9b483ba3674f3ddf56597062ef9955`  
		Last Modified: Thu, 11 Jan 2024 09:11:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e887f4cc821dc6d222f2f7c546d336a649760539871e2576cc534f9545366`  
		Last Modified: Thu, 11 Jan 2024 09:21:34 GMT  
		Size: 12.4 MB (12393697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d62d5b54585b87520b8b2295b12970325a3ff0850b68c2b838ee400b718dc`  
		Last Modified: Thu, 11 Jan 2024 09:21:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec3914d09838b0ccc456c9d07b02b4b1c771a0a32358334f2e836701c5c9472`  
		Last Modified: Thu, 11 Jan 2024 09:22:27 GMT  
		Size: 28.3 MB (28332628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80b9890e5c7940879cabd3a6709c3c04287209cc38ce90a7632b2ea8911d053`  
		Last Modified: Thu, 11 Jan 2024 09:22:20 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba0cee97ab83b737501f2cf462fffc5392cba4e8667fdc37e57fefc4f960355`  
		Last Modified: Thu, 11 Jan 2024 09:22:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67fe22d08da35c74dc2837500e866d3f58441c801eb7b362c5d47d4e2964d0a`  
		Last Modified: Thu, 11 Jan 2024 09:22:20 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbeca2f0bb51e1d543e95b20df9330d46a95674823a2ba8abad90a9f6d87db`  
		Last Modified: Thu, 11 Jan 2024 19:13:52 GMT  
		Size: 3.3 MB (3270159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5a9f392d8331820ace2fddda240262266f3cf8d643d1cb642e0d0ca0d3fae`  
		Last Modified: Thu, 11 Jan 2024 19:13:51 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301e9075015cf2312d3e44114f3cbba29311875ae7c492cb7c585817e1a83926`  
		Last Modified: Thu, 11 Jan 2024 19:13:55 GMT  
		Size: 13.0 MB (13004127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27430dfce5630220d043eb79320f82cdec4a34145d18fd49994a4dac97b430d9`  
		Last Modified: Thu, 11 Jan 2024 19:13:51 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b423cab3c793e38264020c11cc065c55b12b05322c9db00b1c7a56a3cd0afc`  
		Last Modified: Thu, 11 Jan 2024 19:13:51 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; mips64le

```console
$ docker pull phpmyadmin@sha256:171fe471ee3519a3bd1cf3f3e9549d1313104699a722aeb74450007aa156e220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163995451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c00d28c20c25771a23e8253282a010a8d5be4c3a140e2b238b1563e5b61c21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:54:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:54:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:56:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:56:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:56:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:57:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:57:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:57:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 11:09:35 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 13:10:27 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 13:10:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 13:10:34 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 13:11:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 13:11:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 13:57:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 13:57:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 13:58:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 13:58:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 13:58:11 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 13:58:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 13:58:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 13:58:25 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 13:58:29 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 22:28:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 22:28:17 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 22:28:21 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 22:28:24 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 22:28:28 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 22:28:32 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 22:28:38 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 22:28:41 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 22:28:45 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 22:28:48 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 22:28:52 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 22:29:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 22:30:00 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 22:30:04 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 22:30:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 22:30:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5f2517ff42be384eb558d6a81a0390056f5b8d067d23691f856b23666e7d65`  
		Last Modified: Thu, 11 Jan 2024 17:15:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae7428de622829c9eff2ef5b5f84e0c357d18dc2086f7c2bcff4b6e61aff83`  
		Last Modified: Thu, 11 Jan 2024 17:16:52 GMT  
		Size: 80.7 MB (80668646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e5adf5cd722abe2c489e7bedbd4cc9f14c42e9618b11016de723aba16dd551`  
		Last Modified: Thu, 11 Jan 2024 17:15:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6065caa3a69d7ff2dd4838849d371f624c09ba89e10733de5494ac3da244778`  
		Last Modified: Thu, 11 Jan 2024 17:31:41 GMT  
		Size: 12.2 MB (12187692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaad59ffb5698b5f5bdc678e63ef620766721495da511efca28e89f5413e1bfd`  
		Last Modified: Thu, 11 Jan 2024 17:31:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758c07b6cf4609982a29d7a76bc89962b3ad01b41c8a45466bbb1c51bdee6168`  
		Last Modified: Thu, 11 Jan 2024 17:33:09 GMT  
		Size: 26.7 MB (26698872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495bdb782f85cb7a0c1be74cccab13fd07710a50031575dbff62e345fc9ba2d7`  
		Last Modified: Thu, 11 Jan 2024 17:32:53 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0e55d1adaec28d4ba54ddd8ee5c1e066dbf76bfd5f8d87395927cfeda0c09f`  
		Last Modified: Thu, 11 Jan 2024 17:32:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801bfe0c5eefe6b708b6955c1a72294000094ae20befc46483673ad38d2d34f`  
		Last Modified: Thu, 11 Jan 2024 17:32:52 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490e504a6482dc966b7557ffede4046318d88da7fa5746ecf32d629fb3e276e8`  
		Last Modified: Thu, 11 Jan 2024 22:31:16 GMT  
		Size: 2.5 MB (2511872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb724c71de3b60f1fe05a2e2e6b9d8032556da4f0493725fc6e5cbe27befe4d`  
		Last Modified: Thu, 11 Jan 2024 22:31:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e78e03f4c22e87d5af19bf86b4d6fe33162c6e7dd99b0d06f18a101373bf9e`  
		Last Modified: Thu, 11 Jan 2024 22:31:25 GMT  
		Size: 12.8 MB (12791200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d9c721232b24aebef638126e97a25fc2e101cf9c482380ae950d122b06f72`  
		Last Modified: Thu, 11 Jan 2024 22:31:14 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853989f5393031af01b6ad480784fb932dc06daebf750894b62d0384753c2bb7`  
		Last Modified: Thu, 11 Jan 2024 22:31:14 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; ppc64le

```console
$ docker pull phpmyadmin@sha256:b11cf6b16fdbd950f408bdb35253d87f1bcf97af4ee9ab600621259483e9a00f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193864276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50dfc1882d72045d1e1e0f2c8e0e60f26ac304dbd8fe63d087d3c0c198d17c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:20:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 04:20:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 04:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:21:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 04:21:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 04:21:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:21:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:21:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 05:18:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 05:46:01 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 05:46:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 05:46:02 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 05:46:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 05:46:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:57:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 05:57:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:57:24 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 05:57:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 05:57:25 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 05:57:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 05:57:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 05:57:28 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 05:57:28 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 14:41:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 14:41:36 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 14:41:37 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 14:41:37 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 14:41:37 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 14:41:38 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 14:41:39 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 14:41:40 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 14:41:40 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 14:41:41 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 14:41:41 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 14:42:38 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 14:42:39 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 14:42:40 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 14:42:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 14:42:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41deccbdb3118a70cea029f0aa9a00e20f50a0f9e7ee48c0b2e47e908baa1aa9`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b1fe163bf5146471d387e12d2994c0200954be8c29360da9b7d6645856db5d`  
		Last Modified: Thu, 11 Jan 2024 06:47:21 GMT  
		Size: 103.3 MB (103321106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21810f5c2e4eb5e038fb75e5935cd7ee106a1f1c2af8465b5b414700d1cbc42`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265d8d0fa8543f42a75533316d3d4e04fd8061097c837a59b30ba983428d4f14`  
		Last Modified: Thu, 11 Jan 2024 06:56:50 GMT  
		Size: 12.4 MB (12393959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef1dbd824e1cb5749b14a8d8005d7adba5f87c1570fee93421f6c4074cc32f3`  
		Last Modified: Thu, 11 Jan 2024 06:56:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99186c0072e6f068550e4a015ea2de788da9904b0f8a2996dd40ca5b47f1b87b`  
		Last Modified: Thu, 11 Jan 2024 06:57:42 GMT  
		Size: 28.9 MB (28874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1d9ac57806f97de7358edaddd1f768ac03f6dfdd4135b0c58b1dadcd45a8f9`  
		Last Modified: Thu, 11 Jan 2024 06:57:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76e1ad25d19b41f16726d99e8d7c64919258418232631ed37b83e42a4817791`  
		Last Modified: Thu, 11 Jan 2024 06:57:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6d1d894e0e404d8077dae0fc68650211c846e57903c34625e19ad148b0063b`  
		Last Modified: Thu, 11 Jan 2024 06:57:37 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660f2726a7c3d27e92f266384ff54e7b3bf7b16f575c87101def87f174d92678`  
		Last Modified: Thu, 11 Jan 2024 14:43:34 GMT  
		Size: 3.1 MB (3133697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf006d65b87f2da9cc524156373edbff85b97abdbcc7767fd9cf04dc97ac246d`  
		Last Modified: Thu, 11 Jan 2024 14:43:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2c03d4abf6eed72af5c18877b5f80e15b77e8cc77d0ac231d40af6857c5b1b`  
		Last Modified: Thu, 11 Jan 2024 14:43:36 GMT  
		Size: 13.0 MB (13004228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d06d948c54292039db91d7dab5d8fb41617275a98c13aa68d0cb27b545b89`  
		Last Modified: Thu, 11 Jan 2024 14:43:33 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26528f5824dcf8db85dfa658c7681adc44eccd760e2188e83bbc735be055b7ad`  
		Last Modified: Thu, 11 Jan 2024 14:43:33 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `phpmyadmin:5-fpm` - linux; s390x

```console
$ docker pull phpmyadmin@sha256:15b0a558ec12e521cc835ef9abbef1910edb1ef11212ce4aac297374f422b28c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163181386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08eaa3dc42af0ba8ead6e17892450a223844e1036771409f1a2d253e1ebd872`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:22:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:22:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:22:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:22:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:22:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:22:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:22:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 07:09:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jan 2024 07:31:24 GMT
ENV PHP_VERSION=8.2.14
# Thu, 11 Jan 2024 07:31:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.14.tar.xz.asc
# Thu, 11 Jan 2024 07:31:24 GMT
ENV PHP_SHA256=763ecd39fcf51c3815af6ef6e43fa9aa0d0bd8e5a615009e5f4780c92705f583
# Thu, 11 Jan 2024 07:31:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 07:31:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:39:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 07:39:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:39:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 07:39:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 07:39:42 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 07:39:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Jan 2024 07:39:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jan 2024 07:39:43 GMT
EXPOSE 9000
# Thu, 11 Jan 2024 07:39:43 GMT
CMD ["php-fpm"]
# Thu, 11 Jan 2024 09:23:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libbz2-dev         libfreetype6-dev         libjpeg-dev         libpng-dev         libwebp-dev         libxpm-dev         libzip-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp --with-xpm;     docker-php-ext-install -j "$(nproc)"         bz2         gd         mysqli         opcache         zip         bcmath     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     extdir="$(php -r 'echo ini_get("extension_dir");')";     ldd "$extdir"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     ldd "$extdir"/*.so | grep -qzv "=> not found" || (echo "Sanity check failed: missing libraries:"; ldd "$extdir"/*.so | grep " => not found"; exit 1);     ldd "$extdir"/*.so | grep -q "libzip.so.* => .*/libzip.so.*" || (echo "Sanity check failed: libzip.so is not referenced"; ldd "$extdir"/*.so; exit 1);     err="$(php --version 3>&1 1>&2 2>&3)";     [ -z "$err" ] || (echo "Sanity check failed: php returned errors; $err"; exit 1;);
# Thu, 11 Jan 2024 09:23:09 GMT
ENV MAX_EXECUTION_TIME=600
# Thu, 11 Jan 2024 09:23:09 GMT
ENV MEMORY_LIMIT=512M
# Thu, 11 Jan 2024 09:23:09 GMT
ENV UPLOAD_LIMIT=2048K
# Thu, 11 Jan 2024 09:23:09 GMT
ENV TZ=UTC
# Thu, 11 Jan 2024 09:23:09 GMT
ENV SESSION_SAVE_PATH=/sessions
# Thu, 11 Jan 2024 09:23:10 GMT
RUN set -ex;         {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > $PHP_INI_DIR/conf.d/opcache-recommended.ini;         {         echo 'session.cookie_httponly=1';         echo 'session.use_strict_mode=1';     } > $PHP_INI_DIR/conf.d/session-strict.ini;         {         echo 'allow_url_fopen=Off';         echo 'max_execution_time=${MAX_EXECUTION_TIME}';         echo 'max_input_vars=10000';         echo 'memory_limit=${MEMORY_LIMIT}';         echo 'post_max_size=${UPLOAD_LIMIT}';         echo 'upload_max_filesize=${UPLOAD_LIMIT}';         echo 'date.timezone=${TZ}';         echo 'session.save_path=${SESSION_SAVE_PATH}';     } > $PHP_INI_DIR/conf.d/phpmyadmin-misc.ini
# Thu, 11 Jan 2024 09:23:10 GMT
ENV VERSION=5.2.1
# Thu, 11 Jan 2024 09:23:10 GMT
ENV SHA256=373f9599dfbd96d6fe75316d5dad189e68c305f297edf42377db9dd6b41b2557
# Thu, 11 Jan 2024 09:23:10 GMT
ENV URL=https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-all-languages.tar.xz
# Thu, 11 Jan 2024 09:23:10 GMT
LABEL org.opencontainers.image.title=Official phpMyAdmin Docker image org.opencontainers.image.description=Run phpMyAdmin with Alpine, Apache and PHP FPM. org.opencontainers.image.authors=The phpMyAdmin Team <developers@phpmyadmin.net> org.opencontainers.image.vendor=phpMyAdmin org.opencontainers.image.documentation=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.version=5.2.1 org.opencontainers.image.url=https://github.com/phpmyadmin/docker#readme org.opencontainers.image.source=https://github.com/phpmyadmin/docker.git
# Thu, 11 Jan 2024 09:23:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         gnupg         dirmngr     ;     mkdir $SESSION_SAVE_PATH;     chmod 1777 $SESSION_SAVE_PATH;     chown www-data:www-data $SESSION_SAVE_PATH;         export GNUPGHOME="$(mktemp -d)";     export GPGKEY="3D06A59ECE730EB71B511C17CE752F178259BD92";     curl -fsSL -o phpMyAdmin.tar.xz $URL;     curl -fsSL -o phpMyAdmin.tar.xz.asc $URL.asc;     echo "$SHA256 *phpMyAdmin.tar.xz" | sha256sum -c -;     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GPGKEY"         || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GPGKEY"         || gpg --batch --keyserver keys.openpgp.org --recv-keys "$GPGKEY";     gpg --batch --verify phpMyAdmin.tar.xz.asc phpMyAdmin.tar.xz;     tar -xf phpMyAdmin.tar.xz -C /var/www/html --strip-components=1;     mkdir -p /var/www/html/tmp;     chown www-data:www-data /var/www/html/tmp;     gpgconf --kill all;     rm -r "$GNUPGHOME" phpMyAdmin.tar.xz phpMyAdmin.tar.xz.asc;     rm -r -v /var/www/html/setup/ /var/www/html/examples/ /var/www/html/js/src/ /var/www/html/babel.config.json /var/www/html/doc/html/_sources/ /var/www/html/RELEASE-DATE-$VERSION /var/www/html/CONTRIBUTING.md;     grep -q -F "'configFile' => ROOT_PATH . 'config.inc.php'," /var/www/html/libraries/vendor_config.php;     sed -i "s@'configFile' => .*@'configFile' => '/etc/phpmyadmin/config.inc.php',@" /var/www/html/libraries/vendor_config.php;     grep -q -F "'configFile' => '/etc/phpmyadmin/config.inc.php'," /var/www/html/libraries/vendor_config.php;     php -l /var/www/html/libraries/vendor_config.php;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:23:22 GMT
COPY file:f697d9b67ffcb023f485f153138036d27b209f81ffe35ce3b93a825c617138cd in /etc/phpmyadmin/config.inc.php 
# Thu, 11 Jan 2024 09:23:22 GMT
COPY file:d8c9f50886f5865fe589f64cb31544582913bb98f2cfa51a8828d71871363ce9 in /docker-entrypoint.sh 
# Thu, 11 Jan 2024 09:23:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 09:23:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970b99384646b14a68f58b4d5f20aa7646bcdb273987830ab94a7d0c52118696`  
		Last Modified: Thu, 11 Jan 2024 08:18:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5937e142a80962f22503718b83e94f9fcb8d1c62fac80dcce04bb7b4061486ba`  
		Last Modified: Thu, 11 Jan 2024 08:18:23 GMT  
		Size: 80.8 MB (80814132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354ae514a5d8229351dc8ed615a4b5ab3427359d88b93956cdc894c5a4a652bd`  
		Last Modified: Thu, 11 Jan 2024 08:18:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4babb0c6333e83a154a110e4009dac68f92472a8f9bf648dde98b1dd3f9c8207`  
		Last Modified: Thu, 11 Jan 2024 08:24:31 GMT  
		Size: 12.4 MB (12392919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03322e69e0ecf75332ac777db2341aa487691f29106e6141d51266b6bbb05330`  
		Last Modified: Thu, 11 Jan 2024 08:24:30 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a110304a1d9a369e35d186046c24b98576a7ba1111149fcdc55421fa68a2c4f5`  
		Last Modified: Thu, 11 Jan 2024 08:25:03 GMT  
		Size: 26.7 MB (26740097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4d0a5e5922d35e2798e8d5f49adb1a02b7046341170e4995bed728959f8e35`  
		Last Modified: Thu, 11 Jan 2024 08:24:59 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557aa7b6387b47fd0c8c6a489843108dc4e3c9c9cabbf87af57f3d42c76ff450`  
		Last Modified: Thu, 11 Jan 2024 08:24:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f31451eab6160305c0c9e24d53ae9d3723142f82f99ac61c499fa5811a26ff`  
		Last Modified: Thu, 11 Jan 2024 08:24:59 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae9153e27fc8d681aa75855832f4e1062e7fed5f14c45d0e3df7ebf70ecc5a`  
		Last Modified: Thu, 11 Jan 2024 09:24:02 GMT  
		Size: 2.7 MB (2722372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2e10aff4845f5be828277dbf7c72fd90f273076bd9c1ea6beb98ac689bd62`  
		Last Modified: Thu, 11 Jan 2024 09:24:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c30a269f625d5d5e002693c345e02e39821abf5b29077f4e0fd803acfa1cad7`  
		Last Modified: Thu, 11 Jan 2024 09:24:04 GMT  
		Size: 13.0 MB (13004180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75812b629839ac74a385dce531003d8d07deec464cfdee391be234bf9c0d5765`  
		Last Modified: Thu, 11 Jan 2024 09:24:02 GMT  
		Size: 1.6 KB (1615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda50566047e1e4ee8bd8f0a925299773543419b2d0f7138e3683fdfa09b8f9b`  
		Last Modified: Thu, 11 Jan 2024 09:24:02 GMT  
		Size: 783.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
