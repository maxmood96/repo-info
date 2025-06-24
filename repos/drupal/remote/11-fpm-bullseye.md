## `drupal:11-fpm-bullseye`

```console
$ docker pull drupal@sha256:461b2828fd0db71f802bfcf1699144b639b73c3add86a8fa63b0554d7fc70ddf
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

### `drupal:11-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:7ee75b1c76d8871c118cc15076d60bc1a154aec5b628b751fc6c95441114932e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187974772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f159f8d4f8c62be4ad6315886b38ace67f6807e2eb1eb1f75c4f9468f3df99e7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323e1100051f380223a5b2672d241ed25ac8c2734438f536c2f06da36c789c19`  
		Last Modified: Tue, 10 Jun 2025 23:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4cdf0af20a44547e190b29fdfa5409941aabac392ce403335e01b341501ace`  
		Last Modified: Tue, 10 Jun 2025 23:33:17 GMT  
		Size: 91.7 MB (91655276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706461ddcf90e13f91ccdf585fb70cc7095524e6722ad6c9c5537bf57da13632`  
		Last Modified: Tue, 10 Jun 2025 23:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cb1437bca5fd7a43c8ee73bb7d2fde7ba2662f99e48567407966ac95fe2f2c`  
		Last Modified: Tue, 10 Jun 2025 23:33:11 GMT  
		Size: 13.7 MB (13723088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67a0dd859a4885c0310249b613c08a0feb7b40edfa0d9b07e696d6cc1cd4a3`  
		Last Modified: Tue, 10 Jun 2025 23:33:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5a6ca6d32b3b6d28d41303821905bfced014ba6803a133c5a5bb16b451ed0`  
		Last Modified: Tue, 10 Jun 2025 23:33:18 GMT  
		Size: 29.0 MB (29018529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722a4ced448c5f9685874cdb1b0db28f2935167fa1fcb78a6b48a77d7910c2aa`  
		Last Modified: Tue, 10 Jun 2025 23:33:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68107eaa44519dc1010b71c113d0532f716f4d7a9771d955e9682ee002932ad`  
		Last Modified: Tue, 10 Jun 2025 23:33:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442067a066212695e6135efcc7524f94b98f1c448d08d45803c0f8d6a61c7f06`  
		Last Modified: Tue, 10 Jun 2025 23:33:11 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e765c997ec989afaea41f379adaa62575a1be758e2a1ea5b3f2dad0fb1af7a5f`  
		Last Modified: Mon, 23 Jun 2025 22:45:19 GMT  
		Size: 2.0 MB (2037844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc55c7b91093658833386883eaf3ba0f1c26601ff2baec9a3d9ce3cda4c6ca7`  
		Last Modified: Mon, 23 Jun 2025 22:45:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b180d2fa99611c8d0281cc33d706b0a5167a8039e15ded56ed5631e57ab447d3`  
		Last Modified: Mon, 23 Jun 2025 22:45:20 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241f7fe343f126888d8e78c19978932840c8dbfb38aeca7c8cafa007a996b725`  
		Last Modified: Mon, 23 Jun 2025 22:45:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0bed12d4bfc68b3eb03515706064514bdb20a2f441efc726f6e8ce9ca27e2`  
		Last Modified: Mon, 23 Jun 2025 22:45:20 GMT  
		Size: 20.5 MB (20517912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:80d2c731f27b009d3549ee69b2f448f13d6b5c80e9d1e242d37bc63e07f88e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6710792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc267093e2ce77a08b1c4e31d5ef0e14fcbc239d29b44248e66b67ffc9d35785`

```dockerfile
```

-	Layers:
	-	`sha256:6b1b051938264c31ada2b987879fa6538b03c39e63b24b4a498c92a42474b3b1`  
		Last Modified: Tue, 24 Jun 2025 02:01:50 GMT  
		Size: 6.7 MB (6675876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab5f55d46dd9a886c46d2c276b3f5cdc759ca54ad3331f31ca965ad2015343e`  
		Last Modified: Tue, 24 Jun 2025 02:01:51 GMT  
		Size: 34.9 KB (34916 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:c115e0e10c9df960e5fe04686ff59ccf143755f2ba9ef2c4b8aa7f56ba91cf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157597733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb44616c5bd381f1a7c2d644c8268f0fcd7a9cb245edc43cbbdf30cdfb3ffa86`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ad6673cebc90ab6de18533ba0930b8c2a04aedaf3fc38e7ad478a5a3bf65fe`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0f6a80aba762784bd149c214bb34433118513f1aaf602bd59a2955c01fc68`  
		Last Modified: Wed, 11 Jun 2025 00:14:18 GMT  
		Size: 69.3 MB (69326502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a6949a51563c9f0a673e97cc2e3ac553e26bf7c6d1701cdc61ffbc4f14be0`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfc43035a18e657e9d70e52c7906dd84a8b862c1192967b08c82fee3e480529`  
		Last Modified: Wed, 11 Jun 2025 00:14:15 GMT  
		Size: 13.7 MB (13721667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22656ef6e28a599eae60f5f99cb8544f9e77b5ba69ca8c641f7602941367286f`  
		Last Modified: Wed, 11 Jun 2025 00:14:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471901952773c742d90d15292e6fc42e750eae65bfc2f943ffc5fe9778a61208`  
		Last Modified: Wed, 11 Jun 2025 14:32:21 GMT  
		Size: 26.4 MB (26427930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08b9e8a967a18fe410970fbc60c87ebd4ac8d57a1ed00250b5d87512a66f29`  
		Last Modified: Wed, 11 Jun 2025 00:39:51 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03409524a22381dec4d823a1b2b123b54d27c1e06f2d7a69f299ca3fd9b3fbb`  
		Last Modified: Wed, 11 Jun 2025 00:39:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f738afd4cd76790a1f364697990b988dfe953dc8561ccbfd9fbaa2fa28600cd`  
		Last Modified: Wed, 11 Jun 2025 00:39:57 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70e289b5d1c36d669c8854e178c4b533a0e258faa0cff6b4493e39fe64a6c3`  
		Last Modified: Thu, 12 Jun 2025 08:21:57 GMT  
		Size: 1.3 MB (1293622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d8532ec8e4f64735980bb5728a551ca57a2bb1ed70d24e018de096f490a985`  
		Last Modified: Thu, 12 Jun 2025 08:15:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce64f127836764575eea4e35fc0f96d58560cf12b615b59c643c29cf74741873`  
		Last Modified: Thu, 12 Jun 2025 08:18:19 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f8eb50edd0b368cf72b1dcd482629ac0b1ecfad371d11ee29eadf86673ea21`  
		Last Modified: Thu, 12 Jun 2025 08:29:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bd20c63fcf297d064a964dde06e948704810034515e8655b8a3e50611a4aa8`  
		Last Modified: Fri, 20 Jun 2025 22:15:39 GMT  
		Size: 20.5 MB (20517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:23afa12d6e86b181c61c01c77e8d17457bedff30c19eb88aeaeee03235268ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd158a9d60ea2772750e93d45c23b2ad48ac2654c87e3dea8310dd7499667fe`

```dockerfile
```

-	Layers:
	-	`sha256:342d974565ca1617c3de6867be04e660acb9c45c1f5d43485af79ba62299c7ff`  
		Last Modified: Tue, 24 Jun 2025 02:01:57 GMT  
		Size: 6.5 MB (6483584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911e6e9da58bb44e8a2297517308a604c159473cac77fd61510307465725c88f`  
		Last Modified: Tue, 24 Jun 2025 02:01:57 GMT  
		Size: 35.1 KB (35071 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6ac94811aca7abfc42fb9faecc6252e6384922fa57fb224debcb2200368a7460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181316614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e6e98795ac31ce3a65fba290ced82add70e6aee041a70a3332c912be044c2b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65977ff69501a7dc5f6e26302db9f945a47530721a001a3ae4baa1384ea7848f`  
		Last Modified: Wed, 11 Jun 2025 00:44:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82a527151d12965d37878cfa80a9f76151d3f1ea0f4df493f325df37cff3f11`  
		Last Modified: Wed, 11 Jun 2025 00:44:16 GMT  
		Size: 86.9 MB (86941837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363d60d40db13be926f62e34f82e495ebb264495e58500092c9d7d6f3c24cdea`  
		Last Modified: Wed, 11 Jun 2025 00:44:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab52589597c92d8d219267fb2fe4677da80b82f173666b7800ac0152da571a1f`  
		Last Modified: Wed, 11 Jun 2025 00:44:13 GMT  
		Size: 13.7 MB (13722361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed99024308a548802629dac9ce416a99e82cc5e08ba8919a3903f51b4ca706`  
		Last Modified: Wed, 11 Jun 2025 00:44:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc51916b419fc88729a59667fac918a8d24b62854ef79a64778eb8911b5ff0`  
		Last Modified: Wed, 11 Jun 2025 00:46:57 GMT  
		Size: 28.7 MB (28686902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aedc534349a0863a9940821502fda104a26ba8d92f275aa61aa86fdd621681`  
		Last Modified: Wed, 11 Jun 2025 00:46:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a492b6e8a5f73711c6c4cbdf0ce13d8e20cea04449b6cec0d3ad6bf96a681`  
		Last Modified: Wed, 11 Jun 2025 00:46:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307b089e6983f2e3bc5daab002383e26c38f68bee79b76639d8a65fbb3ba9bf`  
		Last Modified: Wed, 11 Jun 2025 00:46:55 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e983a1a6bd64931dc20a8610208300acfc26c9972261548664d8bc7e69542c1`  
		Last Modified: Wed, 11 Jun 2025 18:40:31 GMT  
		Size: 1.9 MB (1936641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2661fcfa471cd3c5e9ee3d37227ebee54b207d9f7fa451a3224ed63fcedfec12`  
		Last Modified: Wed, 11 Jun 2025 18:40:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d048c7a478c99a9055dafe0905ec26028039c480853c30b2ffdd0f11ea15c826`  
		Last Modified: Wed, 11 Jun 2025 18:40:33 GMT  
		Size: 752.8 KB (752767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d1c94bc3235a28c31f014f5669368c2e6dbc78d30b351f237c1f2cf621f529`  
		Last Modified: Wed, 11 Jun 2025 18:40:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c3119db8d4530ed35f68a624811189cc07828534ab2e13cb77e74bef1250ec`  
		Last Modified: Fri, 20 Jun 2025 22:05:24 GMT  
		Size: 20.5 MB (20518636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5134c5c182a06ee7a7614e539540377f870b89836801605a5aa6efeff9832219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e30a73678e6f38d8c0d921abb1aec7fb8ba83afbd9199bda56e55b4b6306c3`

```dockerfile
```

-	Layers:
	-	`sha256:1dab2b38a62c8470a0f39e1ed197e9c552598d7e8cb6fa158d7e67358c4691ae`  
		Last Modified: Tue, 24 Jun 2025 02:02:23 GMT  
		Size: 6.7 MB (6678410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a99c588691618e7bf5adf1a62884220952016337a93b15a30dede1e75c4047`  
		Last Modified: Tue, 24 Jun 2025 02:02:24 GMT  
		Size: 32.9 KB (32926 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:e2d26ff134cdcee2631f68116a938fc6d32add10e1e854273983d06256d9559d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190609586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccc35299df2950270ff1bc4f25010613dadf41692d157d85cabd1cee9d9a537`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Jun 2025 23:47:13 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Jun 2025 23:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_VERSION=8.4.8
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 05 Jun 2025 23:47:13 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Jun 2025 23:47:13 GMT
WORKDIR /var/www/html
# Thu, 05 Jun 2025 23:47:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Jun 2025 23:47:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 23:47:13 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Jun 2025 23:47:13 GMT
CMD ["php-fpm"]
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV DRUPAL_VERSION=11.2.0
# Mon, 23 Jun 2025 20:40:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 23 Jun 2025 20:40:58 GMT
WORKDIR /opt/drupal
# Mon, 23 Jun 2025 20:40:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 23 Jun 2025 20:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f0f5d5a34f14d256e9eae5eaf60af18dd2e37c4c2420aa036307e0add2a45`  
		Last Modified: Tue, 10 Jun 2025 23:33:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad9ddb819f3393b41c4581cac6a5a755f4e140c33e7a38750a7f56e198b9eb0`  
		Last Modified: Tue, 10 Jun 2025 23:33:33 GMT  
		Size: 92.7 MB (92726319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76638029c7d61d14b1e9b43c22f3684b21246f0b78ffd9b6fb030b2b05b9a44e`  
		Last Modified: Tue, 10 Jun 2025 23:33:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d2f8ca8ff3b960851118a29c364073444211b9f56f83f18b96f26e922ea7a9`  
		Last Modified: Tue, 10 Jun 2025 23:33:26 GMT  
		Size: 13.7 MB (13722338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dc10dd5960a583eb34b11cd9858f38c9382aadc816f67f3e81f86a657cb6c4`  
		Last Modified: Tue, 10 Jun 2025 23:33:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e5f1be9fb725a6edc7af6806a7243f8892a605e9073921cefa4797f28435f`  
		Last Modified: Tue, 10 Jun 2025 23:33:27 GMT  
		Size: 29.5 MB (29546253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00356088471129fd7ef37936af3daa8e29c528111e5ccb1a30fec343c55eada`  
		Last Modified: Tue, 10 Jun 2025 23:33:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f21ce2a3eba04fdd2f277fe0dff637254d3732140c0c8a2c66b3080e2d62715`  
		Last Modified: Tue, 10 Jun 2025 23:33:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2f830f8011ff989543bc208a31c68888626ade15ee72bbc35137c7f2cab9a2`  
		Last Modified: Tue, 10 Jun 2025 23:33:24 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365f25faf7c7d31becf0a906e695d41ebac31e1e0c7efa643a9c795bef38ae6c`  
		Last Modified: Mon, 23 Jun 2025 22:45:26 GMT  
		Size: 2.1 MB (2141034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e750dc731cbd40fba6a0506aa677735db74f44b212d48c86fab15694cd40ead3`  
		Last Modified: Mon, 23 Jun 2025 22:45:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8359862a59b50a9b345b99c36d7ea8564de35bdb98440ba55ded8f5957c52`  
		Last Modified: Mon, 23 Jun 2025 22:45:26 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9091a91affe7a78f0af55a0443f71bd98e6a7929a14176cfdb6a1ebf58b89e`  
		Last Modified: Mon, 23 Jun 2025 22:45:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5eda9feebc0863538600eccfa1d27f9155a5f57d452359cf5ee16f82e6bf3d`  
		Last Modified: Mon, 23 Jun 2025 22:45:27 GMT  
		Size: 20.5 MB (20517905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:dcf1fe6580f3cdd85d416c5bfa007091161565cbff745d6de57fec237232ec62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6700874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd321b085ce0c9b80127631a35ca3fb95b0c7342ad3eba3a6955bb304ce6284`

```dockerfile
```

-	Layers:
	-	`sha256:b307d208133c1e92391831aa27ea04476f706be30e0f14448eb85f0b471c1301`  
		Last Modified: Tue, 24 Jun 2025 02:02:40 GMT  
		Size: 6.7 MB (6666021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060b4b46d06afdac9f0c70a37f9ee5260eae5f784db37dc3b2e2a873bef86890`  
		Last Modified: Tue, 24 Jun 2025 02:02:41 GMT  
		Size: 34.9 KB (34853 bytes)  
		MIME: application/vnd.in-toto+json
