## `drupal:fpm`

```console
$ docker pull drupal@sha256:43b07cbb348b2b02363c36840a65625a643d3a17ffbbb096c8a157845565d6bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:fpm` - linux; amd64

```console
$ docker pull drupal@sha256:7e477fc5b44d7e9f88c4bbb850bdeb65ddcee535719b3d5b4498951d5e980a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195830928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d18b398a47887734e2e2694e4411fe82359890d85249dcf3fd9e5c7f8b501`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fb9b2762214328a8c15405411d616c3a0a5165e14e187f6ae11029a528efb2`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6d2e549616e2d235d2c6ee091b5fc89136b4090b6bd83483b36e5ebbf16fb`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 104.3 MB (104345465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2327de212962dc8fb9c183a9cc211cdad285d6831fd3de227c461d946c2cacf4`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5c79ec7697bee203616406de6e2da668b853f5b9a0e5bf062e3dacc84a3fb6`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 12.7 MB (12654325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397611f822e1635fd5a71185e266667285eb763fa1b0df620e650ffbd2568be1`  
		Last Modified: Tue, 04 Feb 2025 04:37:35 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6649c69bdbfa87a468be04c01ed690c68644040f7a6ec3cb9e90a4844ce1879d`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 27.8 MB (27827357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e26b94518e4eeaef60d008ddaac4529c95f312de4d4e6e696829c3940195b21`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051782bf8d5fb8de0af5793bcbe37e02be8929bf321d4967fde92657a4e3fab`  
		Last Modified: Tue, 04 Feb 2025 04:37:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cee8f7af261cbfa7452891ca4e3eb51f8c0c613a0a99e95b7a2280723f633e`  
		Last Modified: Tue, 04 Feb 2025 04:37:37 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebd97b17396f1ef29a2ec8e1f0990ad21910049151e25e608292f73ce513fe3`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 2.0 MB (1976637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6fd768d020ed9e96c1e6a1364d0de3c59e7dbd08cc282f06dd7322404b4e9c`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778abaaa436e49e1235d628d251c7a85e697cc626f73a4ecef8f5952697caa51`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f69fd557509708dbf0fc53f1615639f0ba4d85ed3e186fc056716c25a144c3`  
		Last Modified: Fri, 07 Feb 2025 00:28:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa838a38f8891eacd6d28ffea55629baf3893ca72bfd6789545a4a341dc562`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 20.1 MB (20061222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:53449698382d0ba181df1a9cb6ea792d151ab3e63949650cd1157dc8a3416bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6368174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389d8269d7a39106e2220c81d74723f4ede3a782bc643aa61d5f78a6d487dcd3`

```dockerfile
```

-	Layers:
	-	`sha256:b97f35217828d509766d67712345f66015dd5306b019184a77e93a656c0799f2`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 6.3 MB (6330793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b453c2fdb82b187b2cd9358ee1aa225fd65cf730a025674e74f91af7bb2c27`  
		Last Modified: Fri, 07 Feb 2025 00:28:27 GMT  
		Size: 37.4 KB (37381 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a8a8caf6d49d6d032c15dc6e31d18d7d8acfae8742316904f16000a2254a5549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160284692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850d86cce5c938e79be792172e93d4e88f522a8da27d5d6675a2a3937b874401`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3121bf0a9ad47be9cd9230d76c59964a3c5c2ad428f1f2d5e0ea10c439534`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e514983dd1fb84c6ee305b52a5a3c4aa50f60f471002066ed6c1fc22642b`  
		Last Modified: Tue, 04 Feb 2025 05:09:32 GMT  
		Size: 76.2 MB (76162605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2400437b25b5d1b02d62a06166a2fb642e727da4868737aedeb7e86797c34448`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8802d380b689744f51c695e89bac0642f1f3cc09e9fc306f0245f483421ecbd3`  
		Last Modified: Tue, 04 Feb 2025 06:36:03 GMT  
		Size: 12.7 MB (12652122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfdbad9364884669ce3998d675165698eea1eae0ff4cef913f20a430a7a2a9e`  
		Last Modified: Tue, 04 Feb 2025 06:36:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f84ca7f41711566e10874d5040e19c44a00c888f35eb7c372f1f88d109dc085`  
		Last Modified: Tue, 04 Feb 2025 06:42:56 GMT  
		Size: 25.4 MB (25409128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c21d0e085df4010d12e3c4e20c7479ac5aad94cde0fc4656ee7d9f9290fd17`  
		Last Modified: Tue, 04 Feb 2025 06:42:55 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4794c6cc277a6458e9c8aedf11fc599b0d48f23ec15e031e4c9e3d15cc70ac`  
		Last Modified: Tue, 04 Feb 2025 06:42:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a865caf093683fbe3b837738c71881f8a6c8108ad45eb2bd79f701fb7ced4d`  
		Last Modified: Tue, 04 Feb 2025 06:42:55 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90252f0b0c16c3730d8e73500b960262bd106f2b517e770fe57a269b09c9bc7`  
		Last Modified: Tue, 04 Feb 2025 16:29:21 GMT  
		Size: 1.3 MB (1331479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a19bac9b3cff824de5942822b995cc803788b3f20038fb36dc68198fc3b87`  
		Last Modified: Tue, 04 Feb 2025 16:29:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73fe9daa0ac9527bf37a4bc393e919f367bfbaf7f53fea81f9a8d2d55b86d4`  
		Last Modified: Tue, 04 Feb 2025 16:29:21 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ff22bdaccae254eecc948545f07644608cbe461779a22fcd0126a6fe185a2e`  
		Last Modified: Tue, 04 Feb 2025 16:29:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a12aea7cf1fb023280ccdf392101e94d957efb6c3cda7d56c1fa602881246`  
		Last Modified: Fri, 07 Feb 2025 03:21:48 GMT  
		Size: 20.1 MB (20061201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:c07592b98665ead86ddba9ffe9f1056cb338539e0d28ead17fe13aeceabdcfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6194703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68c09d935cfd81845c43151cf6eafa2a5ca2712bde3527b1366ddfc984b9e0`

```dockerfile
```

-	Layers:
	-	`sha256:de418b7822bdc32629a5e1f30f10dfbe6531d4d1f92c15fad8d0243453d534bf`  
		Last Modified: Fri, 07 Feb 2025 03:21:47 GMT  
		Size: 6.2 MB (6157109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464f4a8e14c4530dae7b31d8ffa5f8597719429d420bac0776807f102767f067`  
		Last Modified: Fri, 07 Feb 2025 03:21:46 GMT  
		Size: 37.6 KB (37594 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:cc3da6cee75920523714fb9084f79a5239da427659a73caee7f2ea5324be440c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189639510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ea68e2927180d53821e3bbde7f4c2d30b11db469e8454583255856841de808`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16d737fb0a30c662d9b2adf51f2dff7d89c28971aed9f2463503588644f91d`  
		Last Modified: Tue, 04 Feb 2025 05:17:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8571b79e8caaac6ec73bed43c061c8744cd39e18a67d9cd17dd79b0d6ea2e1`  
		Last Modified: Tue, 04 Feb 2025 05:17:43 GMT  
		Size: 98.1 MB (98130343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f74dc117b0b71ab00cf12fe8d534cbeab80ebf367380080264b1ddede90d92`  
		Last Modified: Tue, 04 Feb 2025 05:17:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff33863edbc9edff09e1b75c6d06bc519407a567c73ba301e6c025338232b0`  
		Last Modified: Tue, 04 Feb 2025 06:43:30 GMT  
		Size: 12.7 MB (12654177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fbbd997a5057dfb2f1ffbd72b4ed38366e522e986a5f5adfe711ff15a8a8ec`  
		Last Modified: Tue, 04 Feb 2025 06:43:29 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04738b2945b886468e5a193ec0e03b6f7dfe6fb2414f27f962bd10faff410a02`  
		Last Modified: Tue, 04 Feb 2025 06:51:53 GMT  
		Size: 27.8 MB (27763222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ecd82ef72fcfb29a2f9019b18a86d270343e3c1250dfb13461b387de056a1`  
		Last Modified: Tue, 04 Feb 2025 06:51:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fe61828ec3a08100a8a75ab5b32eb1c05beff568110db046d699d27cad6483`  
		Last Modified: Tue, 04 Feb 2025 06:51:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13ee7af481aadc63794ab59b90e37adf7d7ef9781520c9a8e77a836d61e48a5`  
		Last Modified: Tue, 04 Feb 2025 06:51:52 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb2c3be9474d7a34abfbb43ae6b7e77b563b4b672153b143c7467c84f1f4074`  
		Last Modified: Fri, 07 Feb 2025 01:51:26 GMT  
		Size: 2.2 MB (2235997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae5cd6e93723462e2f6239a17c6f05aed53236cbe3f61f60544dc6bf24e3495`  
		Last Modified: Fri, 07 Feb 2025 01:51:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecdf023b267442212124a39f6b860470cacc494f5763b1f420060c8e86075a3`  
		Last Modified: Fri, 07 Feb 2025 01:51:26 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a12ce5ccba71332f2a0dc2d7c1d00b659dbd6b3917a05c66f03de63ab96a80`  
		Last Modified: Fri, 07 Feb 2025 01:51:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cdd9b199101f3c1bd4b25e6f80077b3629cc87394f6ecf969f9256d5cdd16d`  
		Last Modified: Fri, 07 Feb 2025 01:51:27 GMT  
		Size: 20.1 MB (20061271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:c7772d4c723230a2076e53ec1d8ac9d632b27f246ebabe2a23df31f655051c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6408313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc24beac6194b341d12c6fa1dc175d6ebdb09afde16a55569adee4e1499231a9`

```dockerfile
```

-	Layers:
	-	`sha256:3ad9c5d5f779b3d2d1fa4d9de48fbe91540ee732a40850e66a78612a1505f9e7`  
		Last Modified: Fri, 07 Feb 2025 01:51:26 GMT  
		Size: 6.4 MB (6370631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2665fc7f34de49d623dc5056c6ceb663decbd4bb3ee6fd3f3e8d2899a1f34f`  
		Last Modified: Fri, 07 Feb 2025 01:51:25 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm` - linux; 386

```console
$ docker pull drupal@sha256:f047af3402f16df8b9ec6fffc2c9bcd29c59b5114c77d9cdd19a464ccde16a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194533664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7cae382ce820e4a8b648cddb50a62eee1cfe733f016ee1ad8fb94937c447ba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea09fb36a8099f1bcb59bd46c7d715db7cdefb7975374b0711ad22ffc7b23432`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693904ad59bbd2a8798ef195d49e8fbc5ce0a2e6573a884c2d7d28e6ee99b7a3`  
		Last Modified: Tue, 04 Feb 2025 04:37:04 GMT  
		Size: 101.5 MB (101513189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ad2b94d4db4515b71f8fb2531591234c0cf7539976dcfac45251553f6f778`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e62d0fc0b15af05f5f61e2e61d26d488c4d5d8133f6bce5148bc24598c619`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 12.7 MB (12653404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f603b816c1838e02a4e96697b02f4f7231ae56c6df15f4a84c33ffd1ce763fd`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93f61e4b8c60ef4b9e9b569aebb77e67d1ee6fb0a9c98bbde9372f31044f747`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 28.3 MB (28336315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e541abcbf1d075e22aa8a544d489f9729ea8d66bea505786e8a7c8af9d4f3e`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a53fb1986722c767931688948d7b91fec36e9af83fc2636797266f375cf5cfd`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b1bfde8607427823e5899da9ddb5ce7c4a3c27828b6042710d7cb9d89d33c`  
		Last Modified: Tue, 04 Feb 2025 04:37:03 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef79d87427cc514e5272f4333fbae1abb1e453f56f96b1987871cb721783078`  
		Last Modified: Fri, 07 Feb 2025 00:28:43 GMT  
		Size: 2.0 MB (2028646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a82eb2bdff13cd1f90fce360b3fcae39258c41bf23b3787ad7bc0c34dd193`  
		Last Modified: Fri, 07 Feb 2025 00:28:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4ef2fb11f8b5992f06a55aa772580aca4a8af609467ceb477cacfe855942a4`  
		Last Modified: Fri, 07 Feb 2025 00:28:43 GMT  
		Size: 740.4 KB (740355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b584afe96f54ccf52bf5fdb7a26f986404488cb68e5f0d2e63301411f8eead2`  
		Last Modified: Fri, 07 Feb 2025 00:28:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc768bf7d43c0701f988433c7bbc3970f0af69112466fa161153e609356e51ce`  
		Last Modified: Fri, 07 Feb 2025 00:28:44 GMT  
		Size: 20.1 MB (20061031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:15a8bb658fce3fcfe784f14e2e5c55a2f25854a59fa5397b33f6124c9febba04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6348325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77da1221397bd83910970a3b31871acefb6273d3a6f30d1c0e9527b5cac9ba80`

```dockerfile
```

-	Layers:
	-	`sha256:f6b08db416bf0d0f5d3bf043624d6be6295811ab2c2ea745a9ed76ec60020c48`  
		Last Modified: Fri, 07 Feb 2025 00:28:42 GMT  
		Size: 6.3 MB (6311044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b266da088ee690552a9949aa87786692904944ab805bbdd5874bd216578525c`  
		Last Modified: Fri, 07 Feb 2025 00:28:42 GMT  
		Size: 37.3 KB (37281 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm` - linux; ppc64le

```console
$ docker pull drupal@sha256:7cdb902f8e7cc6c1464ec9d8b3190aab84f9441007407141bd68b3b8d7d8fc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199556474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65fcec8d7c937b59bfa5000aab003dc0df8ce6b97c82b75fba34b2198d795f9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 01:38:01 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 05:12:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 05:12:53 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 05:12:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0067b44228754830d3db85d21660c50c325bd6a68620721c48aee3eb265735`  
		Last Modified: Tue, 04 Feb 2025 06:02:14 GMT  
		Size: 12.7 MB (12653811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bedd675dddaffd4ac54bebc3077803848cd19e065d2363de3ea38df425c5d1`  
		Last Modified: Tue, 04 Feb 2025 06:02:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442fcc0d4ee3cac2788459b9dc5b6140ecbaa0d0a967a24d55432988c74de4e`  
		Last Modified: Tue, 04 Feb 2025 06:10:22 GMT  
		Size: 28.9 MB (28886079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b88dbd11378733dc373b026705151d377b98033cf3ca5ac60549cbcd297fd82`  
		Last Modified: Tue, 04 Feb 2025 06:10:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbe1e5dd264a9613dcd3494f9ca0cb40fa1c38440aab7d6fd17ed68f9c53e7c`  
		Last Modified: Tue, 04 Feb 2025 06:10:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8f834ad1bc1cea83b7cfe8b32c8e09ccb3da230f8863da374d94431a7db6f8`  
		Last Modified: Tue, 04 Feb 2025 06:10:21 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb12f50cfeffcde5cfc2c869b83802163b93a5dfe86482dafd8a724b0813a3`  
		Last Modified: Fri, 07 Feb 2025 01:02:51 GMT  
		Size: 1.8 MB (1832992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867aad232afc240fc8de79b317506446fc2632de4a04ca6cec8159f625535e3`  
		Last Modified: Fri, 07 Feb 2025 01:02:50 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a2d9b9e9378f1680293e91c79e91edfada72bfb79b32284ed4f75b549cb3f8`  
		Last Modified: Fri, 07 Feb 2025 01:02:51 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb32f6180cf2d252931f839e0ee7896bbfb98b82b75fb7c6d4c07a20283554b`  
		Last Modified: Fri, 07 Feb 2025 01:02:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fd6c3b09377487590de6ac2b6d955d8753ff6ae03f1b71f2afb9d0e63b4b34`  
		Last Modified: Fri, 07 Feb 2025 01:02:52 GMT  
		Size: 20.1 MB (20061182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:89b03637b465c3ad4be866bfd0ef3dd5c5183772e650bb160448bc719badd36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6356595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad21ee4a6c22ef08baffa7af7d3f949dbc6d0d11ad2b1ffb6b0f36da08611a`

```dockerfile
```

-	Layers:
	-	`sha256:28bfa664b2a9e3d9104ee008abed60ac8c6c3a39b7c740239473be4cd319259b`  
		Last Modified: Fri, 07 Feb 2025 01:02:51 GMT  
		Size: 6.3 MB (6319081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65b1fe5fe3b169affe13159e6deeee11a6fc3d0bf73e9876296c9d40a623965`  
		Last Modified: Fri, 07 Feb 2025 01:02:50 GMT  
		Size: 37.5 KB (37514 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm` - linux; s390x

```console
$ docker pull drupal@sha256:0ff0db20dbc2974d4e370e137a31b4c978caf6ec3cd0359b1569e180d6372ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169595618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff2f7ba5d26695758ad1c40448faa5192b238dcee29398630e49eb17ba8fb25`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 17:19:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_VERSION=8.3.16
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Thu, 16 Jan 2025 17:19:20 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 17:19:20 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 17:19:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 17:19:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 17:19:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 17:19:20 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 05:16:13 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 05:16:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1d54343fdf4189be98bca62d5af4bba69360a111a84090af72c0ba9396bd84`  
		Last Modified: Tue, 04 Feb 2025 06:08:45 GMT  
		Size: 12.7 MB (12652581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ddf30ec4a44bab4aef6e34e4cb700ded326a0e84510c17be2bd428baae3d5`  
		Last Modified: Tue, 04 Feb 2025 06:08:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f860f6051485bceade5172875be371c77cc5f238037378a506f69aa5a754e7`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 26.9 MB (26921925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05189f452a1f81f87353268d939602ecec5aae28ab59b7404665f7a3e7240617`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7818f8df4bca466c625f91cd16c3f8ac75a298f3f6cd2bfed2f2daa93cf54`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34deef4e13cd87f26cb7444f1d8c4f26c604fd5a1a8e0ccb1319f67c0c814cc9`  
		Last Modified: Tue, 04 Feb 2025 06:16:42 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3657a2c96fea3ad9130267750584acdf0ca90a63c899f2a175dd8870b306d3`  
		Last Modified: Fri, 07 Feb 2025 00:59:48 GMT  
		Size: 1.5 MB (1530524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3835289ca44692ec73d2c87e3e1c3d34e179db0ce85ce7dc7db2595155933f32`  
		Last Modified: Fri, 07 Feb 2025 00:59:48 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da7b141103916c79552cb79674faa272e6efa41573a5736abe375f4a000c76f`  
		Last Modified: Fri, 07 Feb 2025 00:59:48 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6382ee7fb9c6bbe1c550304ba1c3748effcaa1af3e65edbf1dc325ef79d34be5`  
		Last Modified: Fri, 07 Feb 2025 00:59:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a6e06f76305ec898449f700810e86663b88a8161850e5ab954d91b2aa3237a`  
		Last Modified: Fri, 07 Feb 2025 00:59:49 GMT  
		Size: 20.1 MB (20061117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:44b6c289d9e1ad487b48160cdac4fd55840894a059dd5a7dfbe855a90b3ffabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19fa7a7c5663674d66b1d5e9be584c96710c2ff8c8059b9542e95500972a44d`

```dockerfile
```

-	Layers:
	-	`sha256:1e8d22f249b1d4593087f19dd489ab3011b2289cc2bb92e6c89e6863b243f21f`  
		Last Modified: Fri, 07 Feb 2025 00:59:47 GMT  
		Size: 6.2 MB (6183531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35e7169efba95b11353e6dbc245252973603c80418b3ac055b13b06ccc649897`  
		Last Modified: Fri, 07 Feb 2025 00:59:47 GMT  
		Size: 37.4 KB (37378 bytes)  
		MIME: application/vnd.in-toto+json
