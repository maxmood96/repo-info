## `drupal:10-fpm-bookworm`

```console
$ docker pull drupal@sha256:8965207e948b3a4ec80b69156d0d6095bdaea4052545baea10cfde9495a35a58
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

### `drupal:10-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:e2e3511a03c069916260fcb22dbb8516328e38d62c805362e947a63a806f29ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197246688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70dcffcb8a3438e0066aed385365ce513a4c4031eda48cdf08bf47843cffbc46`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a835f7a42d41baddef8cccc9691d2066b05ea324071f6cf142265b0a9c11f9`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b95319ddc15769ada221761749d9bac6cf478f1b607081d1c4df587ae074a`  
		Last Modified: Fri, 14 Feb 2025 04:09:15 GMT  
		Size: 104.3 MB (104345517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384ebab55c22169d292567399ac1ccb6154a4b7cf24b98d13b73c543592150c1`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa9a36df35da1ec49278b8cbe66658fb83abec98e7f4c8f6062da4661b70672`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 12.7 MB (12650862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4baa754be4b87920fc4ed230c6c0c0a30be6b90e116aa97965c487dfdfbd0e4`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df0e7a23023d4899b4ab528fc2b2b9d5adacaf963a63ccafb2d466a9b94beed`  
		Last Modified: Fri, 14 Feb 2025 04:09:12 GMT  
		Size: 27.8 MB (27828378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0f7866a10b0eac27c8fa758a35ea7ee93453fd1fad523542da9e75c4f740cd`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a58be0a76dce6cd69be1cf8bf5d336147c302cf9d0cd65af2b61c29bda299`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3f6c4b40f7cfb00a7a4a38559daa24397f523bb9d9ccd0a4443d1bfaa7e19`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7fe16b897743bb41376c910a774a04a092eedbd64a8738b29dd915530345ed`  
		Last Modified: Sat, 15 Feb 2025 07:26:56 GMT  
		Size: 2.0 MB (1976258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009e27ebdfd667da5896a8b59227ee6f3a5e0080331499694b3821f0e94cc11`  
		Last Modified: Sat, 15 Feb 2025 07:26:55 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b03d2d665fbe2511a27f64bd8762c63346eda7a6527f58375552e6cef97803`  
		Last Modified: Sat, 15 Feb 2025 07:26:56 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658413e12333440d4ac79ac47285a352082ce96c83c9ecd93f372fa2bd5c97be`  
		Last Modified: Sat, 15 Feb 2025 07:26:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36e806a8bb34892d61b6ae2ea49e466ec0bce2dbb98cf18649b19b6f5cdc3d5`  
		Last Modified: Sat, 15 Feb 2025 07:27:00 GMT  
		Size: 21.5 MB (21479742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:37221feec285b875e214d0fc2ed17ed091391eab3108bb27ec9318b0073e1355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6360904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cba266b2d70fd4efa4b78faa90a644e8b19356a24a1398ac553dc07c5c80c8f`

```dockerfile
```

-	Layers:
	-	`sha256:a1d0584687db84976cd8f1da86db04c90f593b671a2923d696c6501c89d29b5d`  
		Last Modified: Fri, 14 Feb 2025 23:53:46 GMT  
		Size: 6.3 MB (6324753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92411b79ae43c6df5b92d38b261775fe4c3ea3e707aaa39c128ad9a8662f6f3`  
		Last Modified: Fri, 14 Feb 2025 23:53:46 GMT  
		Size: 36.2 KB (36151 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5395728086ea0499af7693eec8167f5485efe791bc01a14c2008714ed56a942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161697340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ba3f7df897ddfecb2dc7c314899ffb1b5c8f25e9a5607959454c90a557f2a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3121bf0a9ad47be9cd9230d76c59964a3c5c2ad428f1f2d5e0ea10c439534`  
		Last Modified: Tue, 04 Feb 2025 16:46:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e514983dd1fb84c6ee305b52a5a3c4aa50f60f471002066ed6c1fc22642b`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 76.2 MB (76162605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2400437b25b5d1b02d62a06166a2fb642e727da4868737aedeb7e86797c34448`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e6b98178585bd9b5689333326fb2ad1aa645cb46050af13ddd35dea8a63a16`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 12.6 MB (12649108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733164d52b112e327bc18dda8a6a6de6f0623b9458bf043ca9666a367b49c6d0`  
		Last Modified: Fri, 14 Feb 2025 08:25:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3448a9d16bf2b5eaf49dd0ed001828c5022c28e14a2d6637abff2b799dfae4`  
		Last Modified: Fri, 14 Feb 2025 08:43:01 GMT  
		Size: 25.4 MB (25406670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994feab71828e660799df6ebb5afbd400b5bf20a9a2ac6f3872639eb75b4361`  
		Last Modified: Fri, 14 Feb 2025 08:25:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cabdc92daf493570e1c73c4ff5b36e544c57172471a160c0f3dbf8e1b8b73e`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f911a5a823830f2ec9af366586b830ef35d980e4b76d68944bf5b9c559a52a6`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c137db1ed5b22a3a436192325a5fa18b4125c7e007b9eaa8a92c8c74511afd5d`  
		Last Modified: Fri, 14 Feb 2025 12:25:07 GMT  
		Size: 1.3 MB (1331170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25613aa94f221114d7d8062ed9b996bd8257ab2fcd5a3ebebc3d245ddb29a44b`  
		Last Modified: Fri, 14 Feb 2025 12:25:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2411279b51e77158578f41659881cb21c1a6f084450618c95df718efe61f17`  
		Last Modified: Fri, 14 Feb 2025 08:25:29 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4989281d2cd155caeac886d1b815665dfff0b5739bbb454c65d533ad33d8ebc4`  
		Last Modified: Fri, 14 Feb 2025 12:25:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9256975c0b1b05d1d419c53a8fbd3e46a7df9a16edee7513ad995fabb81b8ea1`  
		Last Modified: Fri, 14 Feb 2025 12:25:07 GMT  
		Size: 21.5 MB (21479627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:3bc77055e8de72af7ec103c85d0f6cb12448cf963f319bcc138058c285401883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6186173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4cb3a7795d58a347d0135edf3b477631a0c8a742fc0335b46a200fb24c12e9`

```dockerfile
```

-	Layers:
	-	`sha256:c36512998c6ff9127b6b9576371f3e46279cdad101f95f78958337e1926dd5cc`  
		Last Modified: Fri, 14 Feb 2025 11:53:46 GMT  
		Size: 6.1 MB (6149839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caef0e1ee372bb986932ce45b5478b9af83cac99377a905ee834aa02152c7dd3`  
		Last Modified: Fri, 14 Feb 2025 11:53:46 GMT  
		Size: 36.3 KB (36334 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:23e364825921d011e1d0c870caa2f26173cc7e746789480bbf5d7bc449637382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191054847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a13dac98b676de9132bd6b19aa52ebd88072327c55a87e6088a0ec0a0f7805b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16d737fb0a30c662d9b2adf51f2dff7d89c28971aed9f2463503588644f91d`  
		Last Modified: Tue, 04 Feb 2025 09:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8571b79e8caaac6ec73bed43c061c8744cd39e18a67d9cd17dd79b0d6ea2e1`  
		Last Modified: Tue, 04 Feb 2025 08:59:42 GMT  
		Size: 98.1 MB (98130343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f74dc117b0b71ab00cf12fe8d534cbeab80ebf367380080264b1ddede90d92`  
		Last Modified: Tue, 04 Feb 2025 08:49:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e84a4aa5f6a8ad023b9cf41eef0c612dc0c59b80e89476d98518153fc260956`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 12.7 MB (12650757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5390744736065c110d9874684170bfe263302bab10fd26d66ddd2a00da59146`  
		Last Modified: Fri, 14 Feb 2025 05:43:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274b43ab47f8335a3d05777185a1f87f3daff65f4ae3f31323ce3ef25044af9`  
		Last Modified: Fri, 14 Feb 2025 05:43:12 GMT  
		Size: 27.8 MB (27764170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de6b7fcea796558f95b49a3b27b3ef5d235076afbc4d97da1900e41bee18c2`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791314e52bb0a4b81a450dc905217c88b5f25a8c18190ae7d74be420e465b83`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc232132df406adbc0903764c2b0b366c840c0f0e9363fd89e7a6630d681c6`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09269bc096ca8c23d099a8150e65f541233bb3f9af1e5e9b24d49dd4aeac8f40`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 2.2 MB (2235328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88611a61884cf10e1d724daaec9ea9d8290cc4da06248bd9ee49abd2f8535996`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a1cf9acdb761af5446cc94699b0f7bfefda1c88f86598fb529f6859e6714da`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525cbf1fcccc51e7e36149e9aa2cd3b5b927fce056bea9dfbb8166dea91f60c3`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e42780d2eecdab04a61424c21a4954bd37ccb968b0513f7065373ab101bd0`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 21.5 MB (21479737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:7fa3f999eaf19ea140be427a1a3f1c6ebd400dc2338347e5b3113c6af31fed0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1020e5cdeba22c3986d51f424be1ea573d4c7ded5423117919440c7bcae7659`

```dockerfile
```

-	Layers:
	-	`sha256:e90baaedcbfb1e5f9500baef7cd525486abc459ae57b39a6b69569d26605e48c`  
		Last Modified: Fri, 14 Feb 2025 08:54:20 GMT  
		Size: 6.4 MB (6363345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0930f9e0566aa599220e1f035b26e1af74a2221c59ff8d932b86d1c3875055`  
		Last Modified: Fri, 14 Feb 2025 08:54:20 GMT  
		Size: 36.4 KB (36401 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:61347667ed37c22517493c21e594d8760e99a263ce9f0ac409f7ac9c002cdca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195948758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f08f85d9fbd139523cfc2d9b66360e8afbc00bf168175ab9724199bc7df1637`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12872977850b0f276e580892b46396c8ea6a19e5ac26c2c1f22646e1be268ff0`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e33d62dea93b8ebbd742701712d1ead00fc01a5f6ce322e2c1329250185424f`  
		Last Modified: Fri, 14 Feb 2025 04:09:05 GMT  
		Size: 101.5 MB (101513546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa77dcfa2c3fb90c8b1765c294b68f28bfd5f98814a904906b8428e80df796f`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83346b840b46240564bf6fbc38fb3939866e4f984d0d2f48380916159401a431`  
		Last Modified: Fri, 14 Feb 2025 04:09:02 GMT  
		Size: 12.7 MB (12650026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1db055f06b3a2e10c0fbad724fcb5e5c8155032236c58af4a6f5e7f1035c46`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0791dbd231f933b67d7e8316958c1ad0163c5e06cb99235f0a9b9aff8883f590`  
		Last Modified: Fri, 14 Feb 2025 04:09:02 GMT  
		Size: 28.3 MB (28336016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c268b81ae5871a95d4f7453d9a038ceee09a68b203d0cd7f96824c863213c4`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2917cd230c109a452aa7afb6e103f9a264f33b3765c717114575a7e85dd2e38c`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6fae92eb9e9dbc707f15e5f92fa51981c2fb806b9afc39ff6a892d0015e76`  
		Last Modified: Fri, 14 Feb 2025 04:09:00 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4f21c999e18d944759b274625cbe3f7fe030195d597075937012f18021ea7`  
		Last Modified: Fri, 14 Feb 2025 21:14:40 GMT  
		Size: 2.0 MB (2028527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5c28cb9d30b801fb4a584f34f1f9859b777da2bb0597509278941e2ff8baa`  
		Last Modified: Fri, 14 Feb 2025 21:14:40 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8742410016245ee498032cbf40474b83371a37bda2b2d24bd7a7eacefd661f4`  
		Last Modified: Fri, 14 Feb 2025 22:34:29 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b328f3b9709c2c0c8ee677f798425efb548d8966d249c8f603a931fc09744c`  
		Last Modified: Fri, 14 Feb 2025 21:14:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43da4de22d696feaf4d8779c3a60115a0ba48f8229f6d5aea3542a14aa54c00`  
		Last Modified: Fri, 14 Feb 2025 21:14:45 GMT  
		Size: 21.5 MB (21479553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:a80ffdb784d145c3736d9e189a37d1da8824e3c0eaab44a827629d971301996d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18622b1f2a8f1ecbb844de1d1f814007df4a07d8d19a1ccd7994679a52f2656a`

```dockerfile
```

-	Layers:
	-	`sha256:0ba3df9bce005e592aa550bb5a72de1c275c36849330cd1b625b8a3368946809`  
		Last Modified: Fri, 14 Feb 2025 23:53:54 GMT  
		Size: 6.3 MB (6305024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b9a820aca4ef4b4f779042740f74be49c0d8baa5e0c3ba8ecfc967db46107d`  
		Last Modified: Fri, 14 Feb 2025 23:53:54 GMT  
		Size: 36.1 KB (36067 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:93c74723e341caea7dc5429786533a2cbef996689b2d6d1ae39c2d7cec344f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200972449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dccf250f5d24e7fbdd85604a7ca5a41ea85796bee018d625dc86e21ec4165ee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 09:24:12 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 23:02:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3857772b0c96da7c9040613a926250a833d047c55388687562c3a7d4bade07`  
		Last Modified: Fri, 14 Feb 2025 05:43:14 GMT  
		Size: 12.7 MB (12650389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b441b884047b59d4fd27bf4cd9cf16f27889216b492e231cd2ea7aefb1b1bd7`  
		Last Modified: Fri, 14 Feb 2025 05:43:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dfa87f0abe83e32c29ea15e4f19a418a3e76355f47bb03f92e940505f5de0f`  
		Last Modified: Fri, 14 Feb 2025 05:43:16 GMT  
		Size: 28.9 MB (28887389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7b81fee13d1ee02628064f2954bd8c536b8ad4cd8f1dcd813f9198f807eda`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2aab62346be1c6d9980fe0d13b8f7341be8f92b51b6de3e363a9acc4b7d959`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aaabe270a1213cf3832121d82ef465cf4d765a49a13d90f7a7cdb8c74941af`  
		Last Modified: Fri, 14 Feb 2025 05:43:18 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3673ea3d954430bffc870a61cfeecc2e6517370f61c5c1daa036fc06bb1557d`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 1.8 MB (1832640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc806c41e721fb87677acf8e1c6ff6bb5ab7796e19368b192150cf0df87d6322`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d4657512035700796076acd81a6c3fd04ed248aaa03142e68b75de13eff4ac`  
		Last Modified: Fri, 14 Feb 2025 10:11:59 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721caf828f3319b6385ec53d4131c02042e4ff4ecc0cb40dfd8745035b150792`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0de8f0fbcbae4e2be9585f4376bcf07de5faf12b7c3f0451f5ad864d72af109`  
		Last Modified: Fri, 14 Feb 2025 10:11:59 GMT  
		Size: 21.5 MB (21479616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:465e64e3b74e5bdc4edac1e4c02d7db79fc594e92f76ccd53ab283ef36b407e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6348076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b21530c91c5eb655723c5db93a020faf346890aa1970ab2bb8181919e32cf7d`

```dockerfile
```

-	Layers:
	-	`sha256:377112b6a60206513029c970837791184bade176ecc3efa3ff30c2353278e723`  
		Last Modified: Sat, 15 Feb 2025 05:53:35 GMT  
		Size: 6.3 MB (6311819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5daaaabaae2cb55132b4d7ed895d8be664c2c670d5122f945f630073649dc9f0`  
		Last Modified: Sat, 15 Feb 2025 05:53:35 GMT  
		Size: 36.3 KB (36257 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:9e40e2c47b39f42a3d43fe48f9a60263f132b6bd21f0104a22e629b2c4a58fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171011424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2445b36f915089f64512e8e878b3c2dcd2d4981ec28bcfe666894ea7cd29988`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 04:56:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Feb 2025 04:56:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 06 Feb 2025 04:56:28 GMT
CMD ["php-fpm"]
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV DRUPAL_VERSION=10.4.2
# Thu, 06 Feb 2025 04:56:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 04:56:28 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 04:56:28 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 04:56:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 12:11:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 09:33:36 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 16:01:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07346811c939a9e11a4fe2f58e9438ba90b45b4ce156f20ec078bd54e2b54cb`  
		Last Modified: Fri, 14 Feb 2025 09:09:36 GMT  
		Size: 12.6 MB (12649497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7650c5088622ee1e58bd43695c502f40e131d373bf3c9ef4425952b62dcca1a`  
		Last Modified: Fri, 14 Feb 2025 09:09:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebad4598ab0e76f0ff3bc4948d7ea452b1e9f4ca43d046d12be2649246cc8bac`  
		Last Modified: Fri, 14 Feb 2025 09:11:47 GMT  
		Size: 26.9 MB (26922389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911ed057623ecd97050be116d101cff86c15bbb6eea3399bb34fe0253c265504`  
		Last Modified: Fri, 14 Feb 2025 09:11:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a04827cb1014d82ae9b9386eb0306e422f7c0ad29d73ba71312912b8a41d01`  
		Last Modified: Fri, 14 Feb 2025 09:11:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daddfc183acdcf860bb38894ea164627b48e1a5e3dda8eb6c6baeb2829981489`  
		Last Modified: Fri, 14 Feb 2025 09:11:46 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b3fe884d7b9ee5074c39cbaceb47a4cea7b2db603dfe28c4c22cf130e3ada8`  
		Last Modified: Fri, 14 Feb 2025 12:25:08 GMT  
		Size: 1.5 MB (1530183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb2d12b7f4c1229cb83e7701360353b4a550a4683fce1155be0822ce04ced73`  
		Last Modified: Fri, 14 Feb 2025 12:25:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bf0509ad783c6e3ceec9118d868edc160a871c099cbf8bd53a1f07bf183332`  
		Last Modified: Fri, 14 Feb 2025 12:25:08 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ca4876735e8ce5331f926a593a759f43fbe80899b79863573eae56f32d64bc`  
		Last Modified: Fri, 14 Feb 2025 12:25:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82522fa8c296cca3478e454754c28b468fc8846039a28f68d683eaaedc5d1f93`  
		Last Modified: Fri, 14 Feb 2025 12:25:09 GMT  
		Size: 21.5 MB (21479875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:49fb6bb562993aa45f3b02a16805272b3989e31e59bf5ac740b2c9913b5457a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6212439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6c2dff652053eee859002352336596f9ea6448d5c685f746c944c70871f149`

```dockerfile
```

-	Layers:
	-	`sha256:718ce9415f5bfca2edcb211db256b260107e03912de5d09bb0f69d536c1a4c0d`  
		Last Modified: Fri, 14 Feb 2025 11:53:58 GMT  
		Size: 6.2 MB (6176293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62db955dee5ba78bdba8926de0cef1785d0852c7cbf6c4969d637f71be83a0f5`  
		Last Modified: Fri, 14 Feb 2025 11:53:58 GMT  
		Size: 36.1 KB (36146 bytes)  
		MIME: application/vnd.in-toto+json
