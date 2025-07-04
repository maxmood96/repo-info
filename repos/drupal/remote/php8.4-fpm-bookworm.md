## `drupal:php8.4-fpm-bookworm`

```console
$ docker pull drupal@sha256:5f61bbf691c57146f6e922939dd74dde2ea6fc3a44ddaaeef41f86dfedfb0054
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

### `drupal:php8.4-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:ec86a91592a8876480ed9d8d1f0236e7e39eb57a8e09bf4820fd7963d810eace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199979947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328ecbd8dbc20c7901218064744376d7edd7519d4ca576c8f742d7bd86f80ffb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eb609875faf51e20c0ced671506012769a509c263093fc793d0aae0bcc9b5b`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d37056d6f96cf7b814a7f1ca86076762eb6ce3d754ce2d409ed5e7798bd205f`  
		Last Modified: Thu, 03 Jul 2025 23:11:26 GMT  
		Size: 104.3 MB (104331365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b706c5b46fcda02acc967808b0d7b32b6118277430facedae20f1553c8b5b22`  
		Last Modified: Thu, 03 Jul 2025 23:00:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3aa702e2e2e7b76eaa04fd4718ac7b057080d8ea020349787d21e0bd35255f`  
		Last Modified: Thu, 03 Jul 2025 23:00:03 GMT  
		Size: 13.7 MB (13735529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69053dd3f2c3a006bac8dbe50438d79d707d5c85e6b7df96f5cc5f00152000`  
		Last Modified: Thu, 03 Jul 2025 23:00:02 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80656f29d0a8ac69084da01e2f2931ea91139c2f7104f4065a5a5f90c6d59da8`  
		Last Modified: Thu, 03 Jul 2025 23:00:05 GMT  
		Size: 30.3 MB (30289765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a6093d8a355ffe811af742d15ec58bd5453a5f4a0d320999150183409ee79d`  
		Last Modified: Thu, 03 Jul 2025 23:00:02 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53036d16df78c202e7378402ae6cfb39cce0fde375b558f8132e2a2db2f4abd`  
		Last Modified: Thu, 03 Jul 2025 23:00:01 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb9cddaf7dd32a6eee1607b7e8b0fca2ba78e77d5f6d597ad39ce25c291d3f`  
		Last Modified: Thu, 03 Jul 2025 23:00:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7defaa6f49dc318dedddccb9f78b73e11eaff98f593dba1e6996228cb82aa0da`  
		Last Modified: Thu, 03 Jul 2025 23:00:02 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886f0d619830f7927adbf49c2d63648e315bcb7381d8641aea89285d2f655e38`  
		Last Modified: Fri, 04 Jul 2025 00:12:55 GMT  
		Size: 2.1 MB (2106974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11125f628f5e8290155493741208c627fc881c4ba9994b02d0e7aea0f6802da`  
		Last Modified: Fri, 04 Jul 2025 00:12:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfe6ebb1ba5ab1a0a4b58c4848dec98116446e01ec1e1814768462b77f1d8ca`  
		Last Modified: Fri, 04 Jul 2025 00:12:59 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71abe19926df62c531201f5eca2b608dad8aacdefb0ea22999cdf2ffba3de2d6`  
		Last Modified: Fri, 04 Jul 2025 00:12:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a473434752f8010b05840cd006970079e72a9c024ea1c3a8d61ce1b3ce42e1`  
		Last Modified: Fri, 04 Jul 2025 00:13:01 GMT  
		Size: 20.5 MB (20519861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:67cff8967d3246d37af1e7405f04527ee4be8fcf56c556c45c32f560352f92d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6565127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11835fb878a56fa1ca49fc2faf0b524240cfd380e7e649e9ef6e7af976e75947`

```dockerfile
```

-	Layers:
	-	`sha256:78facca5f8e4f67a0426ed756a1cde7574e0ab0895b0fda5225b1b1367bca7af`  
		Last Modified: Fri, 04 Jul 2025 02:02:14 GMT  
		Size: 6.5 MB (6526664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca4d0517767bd236964dcb6a2e834823fc158ab673169eb8298c745b854f289`  
		Last Modified: Fri, 04 Jul 2025 02:02:15 GMT  
		Size: 38.5 KB (38463 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:558d2da8203d636620f2c66013656e74762fd5e20e28ca03083b975feb13b0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164041041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2016409a72e3224ad87b2d2131bddf01ae766d0ee488408ec6425e84151e5d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a170f047a2f100ec1b86f80e383bf503b37a580b5eb1bb420a9d375035706786`  
		Last Modified: Thu, 03 Jul 2025 23:00:32 GMT  
		Size: 13.7 MB (13733302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae84d3dc293911ae400a8bb7b89bf8acdb116fefdca39ecaedc58f8c87955fd9`  
		Last Modified: Thu, 03 Jul 2025 23:00:31 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f8919b5844879a86394693bc28ff658367f9d67d2a3358917c8b26f582d25e`  
		Last Modified: Thu, 03 Jul 2025 23:12:54 GMT  
		Size: 27.6 MB (27590211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef8ea039f3d9086655bdd47dff01f753a6fb7748253cd1489d5f97db238da2f`  
		Last Modified: Thu, 03 Jul 2025 23:12:44 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b298025aab786f6bbdaf45bfcdc41e06e7742b7ab9a68cb488fa0d4eb38cd77`  
		Last Modified: Thu, 03 Jul 2025 23:12:45 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a64de2fb26c65c4fb010b587daaf3db8a184633308d3c663f67c186ed8135`  
		Last Modified: Thu, 03 Jul 2025 23:12:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5214a687f271d2e10d86850e5f8e26d6000ded82744fea036a2a9019674a2ab8`  
		Last Modified: Thu, 03 Jul 2025 23:12:46 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1cc95374d5c0e997e2c7fd8d448876a4961954b970c1cb37ce44d24e5af85`  
		Last Modified: Fri, 04 Jul 2025 05:24:38 GMT  
		Size: 1.3 MB (1342257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a625a9b34f3abcf3f59a7291c9194db8511556c14eedf55036a25add7352ec`  
		Last Modified: Fri, 04 Jul 2025 05:24:38 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba435d77e3e31b82fd80dea281e95eba4f7152962737f4a1e6335c7b7c60a1e4`  
		Last Modified: Fri, 04 Jul 2025 05:24:38 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65ca529d84324b98b5ec27d29419f6c11d114a3cb4e144e60df2ea14850b5d7`  
		Last Modified: Fri, 04 Jul 2025 05:24:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203ca81552171955482a48e1e462c0736ff1d8b6ee913e0b0ada92a9996cfece`  
		Last Modified: Fri, 04 Jul 2025 05:24:41 GMT  
		Size: 20.5 MB (20520579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4cf0ac8f8f0582707416df08da9e7cdfeb2ef2997a18a6f8deb4738b5ac9df34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6378725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b0be5cd174e80449e83fc8cd10ce20fec89fea06cf8184d72541fd6d6b4633`

```dockerfile
```

-	Layers:
	-	`sha256:5b17a7451e392167f629cc92cde6896bfd0ffac874baffde849e18392527ccc4`  
		Last Modified: Fri, 04 Jul 2025 08:01:20 GMT  
		Size: 6.3 MB (6340048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37879e55e8b1dba69159a150b5ba8c7f4ef1f0f18c1d70236a6a49c254102941`  
		Last Modified: Fri, 04 Jul 2025 08:01:20 GMT  
		Size: 38.7 KB (38677 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:783eaad829b36b434738e045fdacda1c2d416930e422f7369fb413c16d3d0c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193149379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e425ac09575c2da43dbdc94c29808133653b78d606ec8aa01d2a2d6e4fc1f523`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f0a25db22853df6a6e6e4155e86895f626a540d37bf7e50bf413fd1fa8f12`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d119d74c86b221b030b9083d0f51ada6b53b7c58ec2a87c7276bf5229a2d16`  
		Last Modified: Thu, 03 Jul 2025 22:57:42 GMT  
		Size: 98.1 MB (98130784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81367bd3a505020af3e40d8bc05177f06efe70245dd3740395c2183000421e42`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40db9b1644f7bfc3518bf0bcf77f7ec471b2fec9ddf66081c3ebebcebe4189c`  
		Last Modified: Thu, 03 Jul 2025 22:57:37 GMT  
		Size: 13.7 MB (13735379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572aa431a09b458148e119d0033c42d1c0b09a1bc71bfd72724c91e964ab51d2`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec275a404d18db939e417c99e7678957566ec0ad36e212c76d510a377d62bb0e`  
		Last Modified: Thu, 03 Jul 2025 23:05:33 GMT  
		Size: 29.9 MB (29909606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d6dfd2ca30d5308f1bbcb151ba13f6eb0e544ac77705ac3fc4c15cd0c0055f`  
		Last Modified: Thu, 03 Jul 2025 23:05:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2578e02c06d7769056836922e6c066c873828c806c0f8997987d7afcfc274bea`  
		Last Modified: Thu, 03 Jul 2025 23:05:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e315b6897a67889d3af7b2b660c06f23ae38528636560878adf8f1c0464124`  
		Last Modified: Thu, 03 Jul 2025 23:05:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d595ed5fdcd840f4fdc12ca878e480ddcf95c2e2e74aaaea8a3f04f8eeecaf1`  
		Last Modified: Thu, 03 Jul 2025 23:05:32 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcf78942a5ae1f8f65999b6f4646e92027a961cbf16497e0624f43d39751458`  
		Last Modified: Fri, 04 Jul 2025 08:23:06 GMT  
		Size: 2.0 MB (2009136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35448c0297ef00f099d32eb6c128afe0da07db17c6a5ab5a7fa7560c53ca5ba`  
		Last Modified: Fri, 04 Jul 2025 08:23:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afec3312d7c150623bf399770f534b83cb123472e6b34e0c683f30a87acbffb1`  
		Last Modified: Fri, 04 Jul 2025 08:23:04 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1fcbf026c9aa9a205cda5e00e759c00958a44e0d2689ff20e69c20a61f9131`  
		Last Modified: Fri, 04 Jul 2025 08:23:04 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a251e8c61e3e26eb0ab2107d81e302b3044dbde242af4665b1cb033502ee6aa`  
		Last Modified: Fri, 04 Jul 2025 08:23:06 GMT  
		Size: 20.5 MB (20520479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:929cfdcbe7cb45877d637de1d3ad89edd9ba2b185347e861f4a1f378a4f5c3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7351c119918aa8e13874d521a634a353260762a018a86f220dcda361beda9`

```dockerfile
```

-	Layers:
	-	`sha256:5d534a0e50f0adc4e07409b8a25e0b2dfa70582c7a96411e95c3ca9dffd00e0e`  
		Last Modified: Fri, 04 Jul 2025 11:01:32 GMT  
		Size: 6.6 MB (6555205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2138b269439915d771ecf2c85bafcd6192c9c8e7c618cb98213cc16e172ff7a4`  
		Last Modified: Fri, 04 Jul 2025 11:01:33 GMT  
		Size: 38.8 KB (38761 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:9b8e53d9ecc0273512b73b0d48b39ddde485ffa3f22a6039455e4672bfee51f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198820151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bb91a43244700a05bb062ffb891dcd2f05a0b1c477522fd10593c8c77179b6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572cf38531581dbdeaa6783ac1a80bb2764bbf9edad76a28f85f12d8f8105526`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde5cd3737079aef0fa1fccfcf1f5132cbb546289d6051af862c93ccf7955dd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:12 GMT  
		Size: 101.5 MB (101515870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8ae3e2f2dafd197ff75f9dbc41498218ee2fcfc83353a28d28a0b99fb2dbc8`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24ae34a95472da417f1cf5d4ea40832722bd49a89e10a288632f47e7a319a0e`  
		Last Modified: Thu, 03 Jul 2025 23:03:07 GMT  
		Size: 13.7 MB (13734540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864cf32ab7e392037717c5af8ca66f252c9965738e190dace6a75f76d6d4bd6f`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9604a875f86d9d51ce0f48350b0524011131a9356ec341c44c8e1ec509b73b`  
		Last Modified: Thu, 03 Jul 2025 23:03:08 GMT  
		Size: 30.9 MB (30872429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a9a7f26e9adcecc92aacb5073088e9b55cf2440a1792b3d156a1d4d4f19531`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669a238a81537d906216c7aa08a1237daec09d25eb57f69bbdd2e0405911a97e`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dc73558f608adb83918629510ed6c08108b70b4c683978ae53baa6641b0e68`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a91cf5245dcf19dddbd7a2a8396c4ebc4d48a59d4fc109d74e62dbedc754577`  
		Last Modified: Thu, 03 Jul 2025 23:03:06 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469bf8c92d94396605a47e987e378b5c5655e251668b59867a8df3dfc275d80`  
		Last Modified: Fri, 04 Jul 2025 00:13:15 GMT  
		Size: 2.2 MB (2199378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3edd75959af09f56ddd15e3d21eb68b6824e6c9c75f11aa3ef205d61dae1ff`  
		Last Modified: Fri, 04 Jul 2025 00:13:14 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47229cc34bba70dd27fb099368412bf724bf1018047b2dbfb9d434db80bc29ee`  
		Last Modified: Fri, 04 Jul 2025 00:13:16 GMT  
		Size: 752.8 KB (752772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb59fdbd0e8e572e722fc788e37b02c2ba89488349e425c24685390f264866c`  
		Last Modified: Fri, 04 Jul 2025 00:13:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbf415aa7fab026f45f1fe1057c66cb466b1a5030217b04636ab22e28788c59`  
		Last Modified: Fri, 04 Jul 2025 00:13:17 GMT  
		Size: 20.5 MB (20519181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:64926b4a6cd9138feb5a54527f3fb28bee32241ce599bad84eee49b4fb462476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6544744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1249fbaca736dd4b6c7be90f9c322d530b25f08dc24a4e09f2d114ebb248456`

```dockerfile
```

-	Layers:
	-	`sha256:c73294bc91bbcb6a3790234d916755036bb98ff64e24baaa084e689cfa07a206`  
		Last Modified: Fri, 04 Jul 2025 02:02:35 GMT  
		Size: 6.5 MB (6506384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59f82e3a236ac084f74a5b4d564e81c53c53c92720a4f408d4c9cc335662321`  
		Last Modified: Fri, 04 Jul 2025 02:02:36 GMT  
		Size: 38.4 KB (38360 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:31d75690e4fc537916243bf0313dd068d5b5a026930b4d68e2d5b3c118253eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203625892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5e7e3439c7768ed9087face282db3d6dbd826c7c4c0702ba4ce685936276`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36b68bed4d5c4fdbbd3f66cf1ee62569453e6d1dea00500a229578b96f8f6c3`  
		Last Modified: Thu, 03 Jul 2025 22:59:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94ede1a54d9ac4e13b34ad1cd441b94ad5436ccfacbf6f1e5deb2957a47257`  
		Last Modified: Thu, 03 Jul 2025 22:59:12 GMT  
		Size: 103.3 MB (103326831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83487f2c5b5e9a02c2d3911052a6efe6e28cc68c5a06b7a0080d8ff6f6a2c72`  
		Last Modified: Thu, 03 Jul 2025 22:59:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bf5c802937165612d2ff5a47ae0e0e4b1879ff0950f03bc9e1014d6093dade`  
		Last Modified: Thu, 03 Jul 2025 22:59:09 GMT  
		Size: 13.7 MB (13734877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3de0b03d0aa86decfd888d050f092a79a6053029494d393d7645346e70e3380`  
		Last Modified: Thu, 03 Jul 2025 22:59:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdbdd5da0fd3463323d6b06371029458ceb7385f17030b5df9f76949482406f`  
		Last Modified: Thu, 03 Jul 2025 23:07:39 GMT  
		Size: 31.4 MB (31356854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b33c61cebc2103d90aad7b924700135634ccd806d80930e4d03259a26ea8548`  
		Last Modified: Thu, 03 Jul 2025 23:07:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c39ff5a5d234beda02ce2eebb7759a9a28e9d2044c9a901890282a2e63e250`  
		Last Modified: Thu, 03 Jul 2025 23:07:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a9d7db11af8c2418bdb5a0227154d4307588cd146a5b2741d77381e10f9c6`  
		Last Modified: Thu, 03 Jul 2025 23:07:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49529b35ef1ac3f2405e6e81f8ac0189ea71b6aff143eb11c51756b20c895b4`  
		Last Modified: Thu, 03 Jul 2025 23:07:36 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b60d86b8f68cf2a741f0a85622d475092fa46da6d2136f983d6cd668733c6`  
		Last Modified: Fri, 04 Jul 2025 06:54:18 GMT  
		Size: 1.8 MB (1848199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420cf5cc3e6f792da6e58837fbcccaaa58d9885376511069210b9efa0b403fb7`  
		Last Modified: Fri, 04 Jul 2025 06:54:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecdb093493c5faba32b39d1bd0e409a3945209fc20034bd03397769b065056e`  
		Last Modified: Fri, 04 Jul 2025 06:54:18 GMT  
		Size: 752.8 KB (752772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a719f3292ac5b6c50b91a34935e1d2a13413b334cd7842437374108c3c2c1b89`  
		Last Modified: Fri, 04 Jul 2025 06:54:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e3a61a1547960207a117067d2c8c52b92e15b1f006da25195ad43b9fab34d0`  
		Last Modified: Fri, 04 Jul 2025 06:54:20 GMT  
		Size: 20.5 MB (20519990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4781e07ba35cb4d22b227493975c671e03c6c945238f06b3386f7d3597a4c06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6542053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc8fca2b447dd3f4b4637e590217bb6f52a656d7bf45b93b44f3ad8d9492a3f`

```dockerfile
```

-	Layers:
	-	`sha256:fd299851ec462f6965d36e4bea0f14e4c89f33f2a577fde1fa704f26a0f6a13b`  
		Last Modified: Fri, 04 Jul 2025 08:01:36 GMT  
		Size: 6.5 MB (6503460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c715ba849b5cca40d634ae3d493f6058579b8f8cf626d61656da3cb8f388649`  
		Last Modified: Fri, 04 Jul 2025 08:01:36 GMT  
		Size: 38.6 KB (38593 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:16470da494ff648dfd295bf3dd11913cd088b4a843ced5f8a6efb2a3b96bccd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173820821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4493b369c3be2cc3d2a6068475174b1a4824c16c34de3469be1b275d54d3f7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 15:58:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 15:58:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.4.10
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 15:58:59 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 15:58:59 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV DRUPAL_VERSION=11.2.2
# Thu, 26 Jun 2025 15:58:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 26 Jun 2025 15:58:59 GMT
WORKDIR /opt/drupal
# Thu, 26 Jun 2025 15:58:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eb609875faf51e20c0ced671506012769a509c263093fc793d0aae0bcc9b5b`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528c62694487a8c0f3520f828eaa12f12ec29ad4944569d71931f79d7011e046`  
		Last Modified: Thu, 03 Jul 2025 22:58:51 GMT  
		Size: 80.8 MB (80825817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc2722da34fe4bf90187950be5838def4ad6dd2e97500d7f8d44fbb460783d`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ca1e21cb0afaa0f1eefa566654879fee5b91b33277cdd5719a002fff279692`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 13.7 MB (13733668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a77212bf8021ec986c0d823a0288d249eb0cb39f4afa671275b32e3e45a1792`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520f8f0b74e206ccbd27c995a5e19c4a100eb025759b1472217ab3dc3bc49287`  
		Last Modified: Thu, 03 Jul 2025 23:07:35 GMT  
		Size: 29.5 MB (29544707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aed2bf4405bd142f856597edce7dc0f975babec62f3c76719df9e1125c717b`  
		Last Modified: Thu, 03 Jul 2025 23:07:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6da932b81068a740c98f8465e67796c9bf074499bb20c8df9aaa26eeba5e2a`  
		Last Modified: Thu, 03 Jul 2025 23:07:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129a98220ed3d5cb85db4919821008210747c6e90271c09d340446379a6a46fa`  
		Last Modified: Thu, 03 Jul 2025 23:07:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0526bbcfca3c6c1a239908576deab130925eb8888b505f7c7cf3440305f3a116`  
		Last Modified: Thu, 03 Jul 2025 23:07:33 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c323e5cc0b28d706196169ef86ed9405f98595399e6b11fc33b05b87f7780a32`  
		Last Modified: Fri, 04 Jul 2025 04:46:02 GMT  
		Size: 1.5 MB (1541846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ec40285f93fe6b45d902cc551c8335031b582baaec504b32a3f234226b068b`  
		Last Modified: Fri, 04 Jul 2025 04:46:01 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850129fd788b40bf28d385e51be512d541a1da7fa5ffb3902070c64ea4027de6`  
		Last Modified: Fri, 04 Jul 2025 04:46:02 GMT  
		Size: 752.8 KB (752768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5cd4f993b82296b026c9991b61ae941934a7774cdc88c284919a6c096d450`  
		Last Modified: Fri, 04 Jul 2025 04:46:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e34c0eb05ae03aef20512f0da782004f115bc8a31b4e6343d6d59d49f1d84f`  
		Last Modified: Fri, 04 Jul 2025 04:46:04 GMT  
		Size: 20.5 MB (20520671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6b871559a02f86e343dc000d008724c81815b49214327761dd68959c5c293995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6402339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8d58b5a63411aabfd57c00eed2b1c3d968b417866b1e2624bdabefe17ded10`

```dockerfile
```

-	Layers:
	-	`sha256:eadbf3d269d1b3aca7e33960e2860bddbe99e9adeb01b33459600d29d264f454`  
		Last Modified: Fri, 04 Jul 2025 08:01:42 GMT  
		Size: 6.4 MB (6363882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5181104c9cf5c7ed9b571b153cfc5a51419ff57704ecf20e3307fcb571dab318`  
		Last Modified: Fri, 04 Jul 2025 08:01:42 GMT  
		Size: 38.5 KB (38457 bytes)  
		MIME: application/vnd.in-toto+json
