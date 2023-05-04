## `drupal:10-fpm`

```console
$ docker pull drupal@sha256:f778e3b50d36ad37dcd9d7a071e62b5e1dab8ead4ca8b448cecafa66da261807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:10-fpm` - linux; amd64

```console
$ docker pull drupal@sha256:4548c19b81812ee49d1440f47986d8e92ac33717dc099279fc2d25f59f39d766
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182403618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf397134c324171679128a4c346309dbe89758317c0b9b0de076d2485f875f54`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 04:37:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 04:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 04:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 04:37:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 04:37:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 04:37:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 05:04:39 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 05:04:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 05:04:39 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 05:04:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 05:04:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 05:14:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 05:14:27 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 05:14:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 05:14:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 05:14:27 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 05:14:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 05:14:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 05:14:28 GMT
EXPOSE 9000
# Wed, 03 May 2023 05:14:28 GMT
CMD ["php-fpm"]
# Thu, 04 May 2023 04:51:08 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:51:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 04:51:08 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 04 May 2023 04:51:08 GMT
ENV DRUPAL_VERSION=10.0.9
# Thu, 04 May 2023 04:51:08 GMT
WORKDIR /opt/drupal
# Thu, 04 May 2023 04:51:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 04 May 2023 04:51:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07353b772b5e325bf0abf03512cfaebe590a14a0858cf0ec2740b5ab055a31a7`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5908153120ba6d8988feadd5f6a8c68a281970ad001ac3be0f5bc9dc030b5c4d`  
		Last Modified: Wed, 03 May 2023 06:51:01 GMT  
		Size: 91.6 MB (91635527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8681ad2eeea6fa7d3aed97bcd471bddff6b4932f405ecb84452c3d2522390e2a`  
		Last Modified: Wed, 03 May 2023 06:50:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8da6caa4e0a7bc8a496934ba729aeb026f020d528b877d81dbd103799c0e3a7`  
		Last Modified: Wed, 03 May 2023 06:53:26 GMT  
		Size: 12.3 MB (12320946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbefe4a49851f53d213b8bac80a7243c4d4c5668fe84ad4d5d295244558df3b4`  
		Last Modified: Wed, 03 May 2023 06:53:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc99b706848707ad19f553cd0d7c1aa0f1d01bae503780cda73948d535bc8b53`  
		Last Modified: Wed, 03 May 2023 06:54:33 GMT  
		Size: 26.5 MB (26530522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687e21a0703d8f95b6842b3e1a1d80ae90357070bb5f4233d3e910972b4a8c8e`  
		Last Modified: Wed, 03 May 2023 06:54:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aa5c0b90b00a81ed26280a55106be51112fa56585f73890041a8bced5db0b6`  
		Last Modified: Wed, 03 May 2023 06:54:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb04bb99b1f302f5866068279f52dff79328f0bf924258c82a1b5a4b85099b`  
		Last Modified: Wed, 03 May 2023 06:54:29 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4ee60d8ec1e8390fa50590e487cf5302f45a23de0617bafeedb51f281c4474`  
		Last Modified: Thu, 04 May 2023 05:12:20 GMT  
		Size: 2.1 MB (2116839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9f866577a126767d7797ea41000392a8a29efac028b2af2770dc4b60433ff3`  
		Last Modified: Thu, 04 May 2023 05:12:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a632bda1fee2c874dc00158fe4f86b545afa407599a651fa2109c7ea5b7dc3fa`  
		Last Modified: Thu, 04 May 2023 05:12:20 GMT  
		Size: 697.5 KB (697534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca0da1899378dc76100090a5386e04961bf8a2d7b238654ba09e54cdad3db73`  
		Last Modified: Thu, 04 May 2023 05:12:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7612bccf5c7dcf8ecf656a82bb724f1ec386e5257dc63e3305eb420b7083c1a0`  
		Last Modified: Thu, 04 May 2023 05:12:24 GMT  
		Size: 17.7 MB (17685406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:10-fpm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:482bb2c03a61acf18841a4dcc17a2159a364aa96c743559d5f2bef1a30d58f11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152349237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a7c1f8526257cc20e5468583044ab4b7b4856a5988bfbcce40dfd423ce99ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 06:02:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 06:02:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 06:02:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 06:02:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 06:02:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 06:02:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:02:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 06:02:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 06:02:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 06:24:01 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 06:24:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 06:24:01 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 06:24:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 06:24:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 06:31:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 06:31:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 06:31:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 06:31:11 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 06:31:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 06:31:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 06:31:11 GMT
EXPOSE 9000
# Wed, 03 May 2023 06:31:11 GMT
CMD ["php-fpm"]
# Thu, 04 May 2023 02:41:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 02:41:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 02:41:20 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 04 May 2023 02:41:20 GMT
ENV DRUPAL_VERSION=10.0.9
# Thu, 04 May 2023 02:41:20 GMT
WORKDIR /opt/drupal
# Thu, 04 May 2023 02:41:32 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 04 May 2023 02:41:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4223092dddf6040b9cb3d66826248ca3c50557af6320203e8a40b6e549bb0f2c`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922e3f7fe606e6c4954d1d9e944c9f9e610ff10a76127e6d51a955e8cc42772b`  
		Last Modified: Wed, 03 May 2023 07:46:36 GMT  
		Size: 69.3 MB (69320181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3bf68a94eff4021eeb6ae2522f556ef8567c37e2fb6f1155469a278208edf3`  
		Last Modified: Wed, 03 May 2023 07:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b37708275b5017d6a7cbcfa137f2cb573c4140eacf468bcba343e9639b65b5d`  
		Last Modified: Wed, 03 May 2023 07:48:51 GMT  
		Size: 12.3 MB (12319419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1ffc9662ab6262b290a0f8ca4754b26398808ab3288fc79fbe1e4bc15826b1`  
		Last Modified: Wed, 03 May 2023 07:48:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bc7e8ae1df914bbff5521931b0205e936af2343c6201a2b8312ba5c6f37823`  
		Last Modified: Wed, 03 May 2023 07:49:58 GMT  
		Size: 24.2 MB (24249184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f171c90962470933a799d9cbd793cc09d4c09e20e260b09f5f790317202244f4`  
		Last Modified: Wed, 03 May 2023 07:49:54 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b34bd182cb03000aff46cabab48238637feaa7482e35c245c3e8608526412`  
		Last Modified: Wed, 03 May 2023 07:49:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cef46eea3bfbd2601b78b7e83adf723e3bffbaa455db2a95126ac09f948c260`  
		Last Modified: Wed, 03 May 2023 07:49:54 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c3b12dd43ab77ac73e7201a1ea1c52f86fa9e07dc844e0598d36290707678f`  
		Last Modified: Thu, 04 May 2023 03:03:10 GMT  
		Size: 1.5 MB (1497650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac5c5619bddd1f55e9ee5894aa7ff538469d25baed72d0c6fd9c4e6e9e5caad`  
		Last Modified: Thu, 04 May 2023 03:03:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4a9dbd3d77f2c3567785fafba2e572739dae849c16bf98d79e4c293f6268c9`  
		Last Modified: Thu, 04 May 2023 03:03:10 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc0e7b8805204b5e9aebf3377f4b5a410794643d777fc6bbd5cca31d080f25b`  
		Last Modified: Thu, 04 May 2023 03:03:10 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db1693b0e61dddec5c32d86cc53ecfd5350a88877900adab0b750e8289bc3a`  
		Last Modified: Thu, 04 May 2023 03:03:16 GMT  
		Size: 17.7 MB (17687306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:10-fpm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:b6e0a6127b3ccf15bb78c9329fae28c7c7032e15f3605f610991712632e52797
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176664899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857d6c3c1d57933ba96b8fac32aa9e541382521975a26b34cf2e9ce2344e9868`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 03:52:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 03:52:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 03:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 03:52:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 03:52:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 03:52:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 04:18:33 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 04:18:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 04:18:33 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 04:18:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 04:18:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 04:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 04:27:33 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 04:27:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 04:27:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 04:27:34 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 04:27:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 04:27:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 04:27:35 GMT
EXPOSE 9000
# Wed, 03 May 2023 04:27:35 GMT
CMD ["php-fpm"]
# Wed, 03 May 2023 23:03:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 23:03:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 03 May 2023 23:03:21 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Wed, 03 May 2023 23:03:21 GMT
ENV DRUPAL_VERSION=10.0.9
# Wed, 03 May 2023 23:03:21 GMT
WORKDIR /opt/drupal
# Wed, 03 May 2023 23:03:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 03 May 2023 23:03:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3582e155c24272674265389c3b317b84bec7ca237a6761ee690aed30a1c5ec9`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313de6edf03aac188b999f642b424cdc014f9f45e218d5ad620a727ef81fa7e1`  
		Last Modified: Wed, 03 May 2023 05:51:02 GMT  
		Size: 86.9 MB (86928311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a576c500430404ceffd53e7ce6f2898b260e011e85c77bdabd75342c1a6a54`  
		Last Modified: Wed, 03 May 2023 05:50:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc3b799473ad37a0be1ad5025e569020d73e99cceccad15f2394b9c6132d49a`  
		Last Modified: Wed, 03 May 2023 05:53:13 GMT  
		Size: 12.3 MB (12320220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee978abbb3a696dc2feefaee000152c4ec9b3352fb65031109fab6612670510`  
		Last Modified: Wed, 03 May 2023 05:53:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65322c00406b6373128c660d16025d0033298dcdffe8e89a00fcd3ec682aeb`  
		Last Modified: Wed, 03 May 2023 05:54:19 GMT  
		Size: 26.6 MB (26583890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc01d450d10ab7a38ed9fe0c07ff704abb3ff8b1f2612bb63cb34f20fc52911`  
		Last Modified: Wed, 03 May 2023 05:54:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16645ea8b8dcdfb25b60e128afc20db28310bbd889580d621d4bfe86dd5bbde`  
		Last Modified: Wed, 03 May 2023 05:54:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919dafe21f086966d8f85544a92e8f10357647e81d8d6029e323536b03f1600e`  
		Last Modified: Wed, 03 May 2023 05:54:16 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe486e98eed80da9445f15b421f16036b9d6e2168e4a5ed57faf17fedad41217`  
		Last Modified: Wed, 03 May 2023 23:26:24 GMT  
		Size: 2.4 MB (2381599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1c5a638430f8a989aaa865425d19b52b03fd2c7098d710258a60aa41efc662`  
		Last Modified: Wed, 03 May 2023 23:26:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d7e109f918ab06b59eab381a235fe6738dc2e479f866e7c5c54a5fe2e63392`  
		Last Modified: Wed, 03 May 2023 23:26:24 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d2eb07e3e90b247cab7a2f6c450cb84623ad09ee98cf485b706bd80291dac7`  
		Last Modified: Wed, 03 May 2023 23:26:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ce905561419f3ee1b27ad44873249900dc9f7e12fa1073a4aa1a8adb8d2667`  
		Last Modified: Wed, 03 May 2023 23:26:27 GMT  
		Size: 17.7 MB (17687286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:10-fpm` - linux; 386

```console
$ docker pull drupal@sha256:72e0d29162a2a3a91e5f299590e6866becfb1b6c03db6ac3e3b28d5bf9cccba3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185032317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a91d5f6f37929b24c35cde21e022389887c899a25bd25fdc43799af2a1890`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 May 2023 00:00:58 GMT
ADD file:caea439e2dbe0148904e3b9a0c5a843d2d0b7c196725d2b41790594e64dcdce8 in / 
# Wed, 03 May 2023 00:00:58 GMT
CMD ["bash"]
# Wed, 03 May 2023 08:55:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 08:55:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 08:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 08:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 08:56:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 08:56:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 08:56:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 08:56:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 08:56:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 09:38:54 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 09:38:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 09:38:54 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 09:39:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 09:39:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 09:54:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 09:54:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 09:54:35 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 09:54:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 09:54:35 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 09:54:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 09:54:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 09:54:36 GMT
EXPOSE 9000
# Wed, 03 May 2023 09:54:36 GMT
CMD ["php-fpm"]
# Thu, 04 May 2023 04:31:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:31:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 04:31:24 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 04 May 2023 04:31:24 GMT
ENV DRUPAL_VERSION=10.0.9
# Thu, 04 May 2023 04:31:24 GMT
WORKDIR /opt/drupal
# Thu, 04 May 2023 04:31:35 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 04 May 2023 04:31:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:10b34014bd1c165cc57a10e7492f17dce658513b7329319fe6c193c85bf752db`  
		Last Modified: Wed, 03 May 2023 00:05:12 GMT  
		Size: 32.4 MB (32388208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e767304c8a25a06c5180cd0487b1d298c8eb93b9276d7f8a33605daeec5deed`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8469e5ef909b43afbcce2cb261155375a3b3f423dadb11383bf91b8d037358f`  
		Last Modified: Wed, 03 May 2023 12:28:07 GMT  
		Size: 92.7 MB (92719962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d946dbb11b755f5978864d6cb1f395dc513c314f5d182df53bd573895bbeb7a5`  
		Last Modified: Wed, 03 May 2023 12:27:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4a2742614c9783a53a97133d8cf472f3b9e414ace3b7081bc7aeb3e2c1e1dd`  
		Last Modified: Wed, 03 May 2023 12:30:47 GMT  
		Size: 12.3 MB (12320179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e067fe61c3296d681309de07d9b5778e30b4fd89d917f3020f658ae44f283c22`  
		Last Modified: Wed, 03 May 2023 12:30:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409011699c0995c627b103c97137db3fcda9bf0ef153ae8e9ae7d0e4e54f3ac3`  
		Last Modified: Wed, 03 May 2023 12:32:01 GMT  
		Size: 27.0 MB (27026041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d1a4725cdc0cf7e946a6d2d224426d53fda5740867363f4214664c843bad0`  
		Last Modified: Wed, 03 May 2023 12:31:55 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a779be8af2956e7afe7bcaec59c25d7db57891e9d03854a10b174dfd7ac4241b`  
		Last Modified: Wed, 03 May 2023 12:31:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c2aad051b9ec1db2db440f77d06056d9b45a55db90042aab5740aa3550e63f`  
		Last Modified: Wed, 03 May 2023 12:31:55 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37989f886bdc94f73826198b95571bb4874a1a14057e222a14911d34cffe282`  
		Last Modified: Thu, 04 May 2023 04:56:00 GMT  
		Size: 2.2 MB (2181492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19afa53d8737984a343233f931ac39cbe68f76ffe3945f8a4ae443c4bcc77364`  
		Last Modified: Thu, 04 May 2023 04:55:59 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbef803c64d01e7146a5b041523fe829e68ea12bddbf2d4802803b2d91d4717`  
		Last Modified: Thu, 04 May 2023 04:55:59 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c58123465150bb481eea4e74b107893a769043a2cf9140771b983653fdd940`  
		Last Modified: Thu, 04 May 2023 04:55:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f894f074cac4127a269be0ede907f4178c5793f908f1ff42f415e4ec735bf`  
		Last Modified: Thu, 04 May 2023 04:56:06 GMT  
		Size: 17.7 MB (17685570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:10-fpm` - linux; ppc64le

```console
$ docker pull drupal@sha256:1b5a5431bebedbecac712c4cd4a0d1203f1c85e29852af907471676fb15f0b67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182237983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c121bdfba8e8444d0ed4b20194b72844c8b3093febc60c584db9fac68d370f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 May 2023 00:31:50 GMT
ADD file:ee3b3c43add645e1a2078f2a6e8544d223abf2754eb8039cbbc2cbdb911b49bb in / 
# Wed, 03 May 2023 00:31:52 GMT
CMD ["bash"]
# Wed, 03 May 2023 06:59:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 06:59:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 07:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 07:00:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 07:00:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 07:00:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 07:00:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 07:00:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 07:00:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 07:20:39 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 07:20:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 07:20:40 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 07:21:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 07:21:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 07:35:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 07:35:19 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 07:35:21 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 07:35:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 07:35:22 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 07:35:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 07:35:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 07:35:25 GMT
EXPOSE 9000
# Wed, 03 May 2023 07:35:26 GMT
CMD ["php-fpm"]
# Thu, 04 May 2023 07:17:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:18:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 07:18:02 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 04 May 2023 07:18:04 GMT
ENV DRUPAL_VERSION=10.0.9
# Thu, 04 May 2023 07:18:06 GMT
WORKDIR /opt/drupal
# Thu, 04 May 2023 07:18:30 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 04 May 2023 07:18:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e39c6de44f96d2720b144cbaa9e763eac60a69222a96279f3962e8a701fb17ac`  
		Last Modified: Wed, 03 May 2023 00:36:56 GMT  
		Size: 35.3 MB (35280910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bccc47384e79d6ab7c10c3eb8337f748e92318727cd43299e1acc121c8a6a3`  
		Last Modified: Wed, 03 May 2023 08:42:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6b95d1f286a638f31ec2a11270e8db85c1c105b3ea97bd589725cbf56207f`  
		Last Modified: Wed, 03 May 2023 08:42:30 GMT  
		Size: 86.6 MB (86634643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b409adc42e9a9872675518e3bd6a1dfe2afc2eb0a918e614a2739abccd4ca062`  
		Last Modified: Wed, 03 May 2023 08:42:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c99b1b51ca0715f371025fc856138a8713957b1250c595e44df0b2327bc891`  
		Last Modified: Wed, 03 May 2023 08:44:05 GMT  
		Size: 12.3 MB (12320954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ef5a81504078d1a213f6386b1ebb9297a0345be95270791ff5525947e541e`  
		Last Modified: Wed, 03 May 2023 08:44:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabdf199f29d61ff4a380310275de3a0f112eb645e228bf20739c35495279942`  
		Last Modified: Wed, 03 May 2023 08:45:27 GMT  
		Size: 27.6 MB (27619173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af38dc3bcb95d387b43175b271f53a65ea7ea4ff0885bdac681f7d11efa3d3dd`  
		Last Modified: Wed, 03 May 2023 08:45:20 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3f2ec8b0933ea02777692a87dd9dd5af306d0a92e1acc7f48a1839ef037405`  
		Last Modified: Wed, 03 May 2023 08:45:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e12b748a9e7ae2b44be03b2910add0fa4b4dacb11265aff25742c1bb16cdb0`  
		Last Modified: Wed, 03 May 2023 08:45:20 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a6aca52c2d036b42be03c141e1583b3e8805ed682bff533e4e3d8f968952bd`  
		Last Modified: Thu, 04 May 2023 07:43:38 GMT  
		Size: 2.0 MB (1983990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4df25e19aaa37786f02a7b4e84b091b9c45f263bdec81d94e70c79f13537a3`  
		Last Modified: Thu, 04 May 2023 07:43:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0c4cbd7303375037b698758d32b7ea6ef8df6bd7fe34d79b8d87d3c8a9c265`  
		Last Modified: Thu, 04 May 2023 07:43:37 GMT  
		Size: 697.5 KB (697534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5965a0310cbe16d328150e2fed2e192be65e9213d5dfc32f072931633398d4`  
		Last Modified: Thu, 04 May 2023 07:43:37 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3311e8dd60a90b8655afdd0c1bbf0a4973e14c764b5bdb2331d81f8fea643f`  
		Last Modified: Thu, 04 May 2023 07:44:12 GMT  
		Size: 17.7 MB (17687445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:10-fpm` - linux; s390x

```console
$ docker pull drupal@sha256:dab61b29b09c8f8893256350a4cb856e2edb57e61471ad10bceb37098654e0b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159277726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bdd89889a87ddc0c82790fce669cb3c01bece7b93770e4a4ccc36cb9ca6a3a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 May 2023 03:41:57 GMT
ADD file:7dcdb7d695d9510a1a7e1623776d63d56f7025bdd1702a13a3acd52af825b9c3 in / 
# Wed, 03 May 2023 03:41:59 GMT
CMD ["bash"]
# Wed, 03 May 2023 12:28:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 May 2023 12:28:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 May 2023 12:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:29:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 May 2023 12:29:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 May 2023 12:29:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 12:29:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 May 2023 12:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 May 2023 12:29:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 May 2023 12:48:59 GMT
ENV PHP_VERSION=8.2.5
# Wed, 03 May 2023 12:49:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.5.tar.xz.asc
# Wed, 03 May 2023 12:49:00 GMT
ENV PHP_SHA256=800738c359b7f1e67e40c22713d2d90276bc85ba1c21b43d99edd43c254c5f76
# Wed, 03 May 2023 12:49:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 May 2023 12:49:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 May 2023 13:02:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 May 2023 13:02:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 May 2023 13:02:24 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 May 2023 13:02:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 May 2023 13:02:25 GMT
WORKDIR /var/www/html
# Wed, 03 May 2023 13:02:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 May 2023 13:02:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 May 2023 13:02:28 GMT
EXPOSE 9000
# Wed, 03 May 2023 13:02:29 GMT
CMD ["php-fpm"]
# Thu, 04 May 2023 07:03:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:03:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 04 May 2023 07:03:48 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 04 May 2023 07:03:48 GMT
ENV DRUPAL_VERSION=10.0.9
# Thu, 04 May 2023 07:03:48 GMT
WORKDIR /opt/drupal
# Thu, 04 May 2023 07:03:57 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 04 May 2023 07:04:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8e4cb8eb5d7a86a02dfc1d3645e982def0fc1c20e1fd14d9c6736177d3887dfa`  
		Last Modified: Wed, 03 May 2023 03:44:59 GMT  
		Size: 29.6 MB (29642157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7039311ef77b804a6867c187f4e31e7b4489fd899d1e33e1be82b55aeec5058`  
		Last Modified: Wed, 03 May 2023 13:55:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f7a91cc134a44679fc67a325a5e92393aabc8331c299c922aa2538945e222c`  
		Last Modified: Wed, 03 May 2023 13:55:52 GMT  
		Size: 71.6 MB (71630105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6562325ea2cb0173d4a5d95a099f62aeddcf32b69d42020e16bb238583a626`  
		Last Modified: Wed, 03 May 2023 13:55:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf92e5d5ae0722e3483178302ebfadc91ad0f991f0d72f0d10ae1f726a07bc3c`  
		Last Modified: Wed, 03 May 2023 13:56:49 GMT  
		Size: 12.3 MB (12319960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770575c6a2ce822abdfcaebbe9a2f65e1adb8a14a187142fd38ae86fab2374e2`  
		Last Modified: Wed, 03 May 2023 13:56:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db9764caf72e2d5ab825d747a4fa4f9373e11f8be004070b53d7813d79a94b4`  
		Last Modified: Wed, 03 May 2023 13:57:29 GMT  
		Size: 25.6 MB (25576144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a83c97725e2e7d1e5527bb6c74a86ea55bfa908fa9904053e3caae6351cddeb`  
		Last Modified: Wed, 03 May 2023 13:57:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796ceb4fcd631e626ba9389334715ab424d215fdabe9e44d5f26bd6b33fd6735`  
		Last Modified: Wed, 03 May 2023 13:57:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e0ddfb577ab287a120dfb1c0969023559f7ee030e47e804714f6ac101db5ee`  
		Last Modified: Wed, 03 May 2023 13:57:25 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6643ae680bbe6a7232f8567fb393b4b7c91d17affe9dec4f6e85f39dce9083de`  
		Last Modified: Thu, 04 May 2023 07:15:54 GMT  
		Size: 1.7 MB (1711194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c651296a0764e05739081a8c7b70a7f02f44af8daa26209beb57d369c1f89c00`  
		Last Modified: Thu, 04 May 2023 07:15:54 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a63b7d8c2f55a1b2db16b57c034430fa7431de19d51ce86d177d34233d7055`  
		Last Modified: Thu, 04 May 2023 07:15:54 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea07990c86b2bf332c80d9c381044e56d81c518099ca654056d5dcb741302594`  
		Last Modified: Thu, 04 May 2023 07:15:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8c3062bf52320b32250c4774461c0892581cf8ecef5cf57f93d5906acc661d`  
		Last Modified: Thu, 04 May 2023 07:15:58 GMT  
		Size: 17.7 MB (17687297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
