## `drupal:fpm-trixie`

```console
$ docker pull drupal@sha256:b5d768628836ce1fdddbe0e156e8899bfdbbdd18d16e8e0da4e51cf3dbbb2c5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:a832753c837e0a20e71e3778892082efd609d465833c44b1a3f40d8cb21448be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198852581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b849671949340958575ab957320387947bbbf0dfc59459021888ddbe7fdfc9f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:08:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:08:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:08:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:08:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:08:55 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:09:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:11:18 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:11:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:11:18 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:11:18 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:11:18 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 20:04:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:04:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:04:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:04:47 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 20:04:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 20:04:47 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 20:04:56 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 20:04:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc77aead35a10f4280d7e62e0c6c87d0d2fb50dbe7ab559afd6017170010d89`  
		Last Modified: Tue, 24 Feb 2026 19:11:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4840eaf8540e542cd0f24033439587164eccaf9a18181ef81928c77e2113a35a`  
		Last Modified: Tue, 24 Feb 2026 19:11:40 GMT  
		Size: 117.8 MB (117842081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d22a0d8d031568ba9597b1881111e78798af9ff3a33af7777bb24d339a167f`  
		Last Modified: Tue, 24 Feb 2026 19:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b8a4ac5ba230791a932dcdd62e4597b42bd44f3fd6498b2007d0cd1edb3e6`  
		Last Modified: Tue, 24 Feb 2026 19:11:38 GMT  
		Size: 13.8 MB (13822173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcf572b1b309cea7b655b2ffedc5e7b98c8138ad480532b03d7ec981123cef8`  
		Last Modified: Tue, 24 Feb 2026 19:11:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3d70b8b9e8702a29b7ced3d39d5aa8790cc55c57ed502bae83ad0633ac600`  
		Last Modified: Tue, 24 Feb 2026 19:11:39 GMT  
		Size: 13.7 MB (13676831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be3c86a4401621f84342b3ad74357665a907b1c44d23e61220bc4ed73bf401a`  
		Last Modified: Tue, 24 Feb 2026 19:11:39 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf83585bf91cafdf39d417d1347d376336ff79ac9581b4eba23d2d453609ca1`  
		Last Modified: Tue, 24 Feb 2026 19:11:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0681cf8d02fa8f16530894f7abea745085aca14abbfe46edb433ea3c62ba9699`  
		Last Modified: Tue, 24 Feb 2026 19:11:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f2901ceed0cc896e27ad86b2bdca6006eefed4f24fad9e41c6709e8cfd6e2`  
		Last Modified: Tue, 24 Feb 2026 19:11:40 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9941ad444ad1e779d6773499b819c32491cb6cbeeaec370b560b4b8bbaca34b5`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 1.6 MB (1634163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba5ab85da940a0837f17deed5c9638e66189c8dcb3e671c3b79e7f72c4525b1`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf1a63726e09d97552be7e22fac77d7029e649165acf1c5d479c0d55d52309`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 777.5 KB (777545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed98a680711ae83be6fb6f84f97f14b4cf71f489a0d33ac121dbc86310acbe6`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01e1e9f14ffe9d13ac9c3c9d37292e9fc885f86df993c22ef03aa19f6467a5a`  
		Last Modified: Tue, 24 Feb 2026 20:05:14 GMT  
		Size: 21.3 MB (21307536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:afbe8c46f11b2f959ac935412199f93f4f8936e0be694df8ecae7ac12e2e208f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6849206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598eecc0650d484dc0cbed419292d747a717e856e445bbf5a2d79ecdc6594a0a`

```dockerfile
```

-	Layers:
	-	`sha256:580952e0bb66f3c6cde70860fa2998eafdf7a707acefe229bcd92504f92a3242`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 6.8 MB (6811051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595c8866d6e2e861fbff6a5bfc65a815be3d2d55741471d7ed4fd4cdeca7c2da`  
		Last Modified: Tue, 24 Feb 2026 20:05:12 GMT  
		Size: 38.2 KB (38155 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6a7c630712509f808a690c24de260ea0c882d427723a158d81de2c06a162f43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161290402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae1434013eb7c6e37858854133f696ca2c79008fca4d81f55a8f62ec8bdfe72`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:33:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:34:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:34:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:34:18 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:34:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:34:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:37:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:37:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:37:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:37:09 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:37:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 18:37:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 18:37:10 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 18:37:10 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 20:13:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 20:13:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 20:13:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:13:47 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 20:13:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 20:13:47 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 20:13:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 20:13:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979ec7fde0c0581c5875c4652f47ca296a8d05ae066abb598d37c007adab8a08`  
		Last Modified: Fri, 13 Feb 2026 18:37:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4c200395f915a909862f7ba26aa331fa7e6f6a82ca68dedc3757afd3f0d94d`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 86.2 MB (86244876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0093fba24f2b024dcb42f26753b78dba580740da85e98e3230371d720b8c6f`  
		Last Modified: Fri, 13 Feb 2026 18:37:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b422916ad98e35b635023754d8d23f08ac127ec3710e421f42fb08bcf3a74e74`  
		Last Modified: Fri, 13 Feb 2026 18:37:26 GMT  
		Size: 13.8 MB (13819571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1c952795135a02460a610520dbdeb251054cc133a6e7ceaa360641ba65a013`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569765b85694b5793c9da73b4dcd349baa90449be6ec03005eb5b6860c89ec12`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 11.6 MB (11568100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04053ca32a86231c7b8a714c48f298d674f5c7b5c493441fbef80813ca5729a`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8037321e7e93613718712c42b93708bccc2f9a55639b29098c4be9ec0e52ad8f`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594546aea187446e6fa48f3a16e8d2d99122d8ee9fa1a25394dadc17776dd683`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd6ff77e47bb9a94f45eba7ba08f58b7eb3db68c1bfd56ac26b01f3479a84e1`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdcc3c107d6d4ac3f5157bce599ceebc91b48391233c128d1f601c3c869551`  
		Last Modified: Fri, 13 Feb 2026 20:14:13 GMT  
		Size: 1.3 MB (1347348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f678bca94f7beca3661585d295eab94efddd6b700f5fbcad0e107ef8386d36b`  
		Last Modified: Fri, 13 Feb 2026 20:14:13 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e715bbcfca1da593c5becc63178581aca63da3f77831b12cb3fc0823c7abceba`  
		Last Modified: Fri, 13 Feb 2026 20:14:13 GMT  
		Size: 777.5 KB (777542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb9045c23a739e4513c7b5590619adfd7b8f317f412e29ef5e1623796c92f63`  
		Last Modified: Fri, 13 Feb 2026 20:14:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9753b666a125eb543db28a8b4eac4b2cd1222efbead18c9887c450fb3cdd68`  
		Last Modified: Fri, 13 Feb 2026 20:14:15 GMT  
		Size: 21.3 MB (21305590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:295d62b47f8bc20be2fc7ad903323b1016f1ce1b63b79dd8e83f0caed2134f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdb423746ccec128f9617451a19a9a66bffcfbcbd5df1761194ec343d61bbbb`

```dockerfile
```

-	Layers:
	-	`sha256:610b6f25b4c102f8d4b7d0bc98aeb71993d66b8154ecc9c57046692072fdeac7`  
		Last Modified: Fri, 13 Feb 2026 20:14:13 GMT  
		Size: 6.6 MB (6614948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8255b2f4f660cec575a86c68720203a9acfc4ce80acf1b11297d0c73ffffb0e9`  
		Last Modified: Fri, 13 Feb 2026 20:14:12 GMT  
		Size: 38.4 KB (38373 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:0fcc9a5b844f418d53b2c0836e7082073cdbd153e9e51f7df6a6d908f208b984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191155878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2f0f706aab15871a3bd0f53842d99ab4575f73a6cf1a717944598811fc6a0c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:12:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:13:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:13:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:13:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:13:06 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:13:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:16:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:16:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:16:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:16:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:16:20 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:16:20 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:16:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:16:20 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:16:20 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 20:15:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:15:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:15:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:15:35 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 20:15:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 20:15:35 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 20:15:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 20:15:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b82126a5a0d8dc4a14e6664f6a3aac03f5a99e39b4e5f76217f8813153ffa`  
		Last Modified: Tue, 24 Feb 2026 19:16:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124827e5c72e8c5de8101df7fb751baff91e882fbd9c527bae4bccef988239a`  
		Last Modified: Tue, 24 Feb 2026 19:16:44 GMT  
		Size: 110.2 MB (110163164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e4f626d6c9dcb55a517e42a61e10e7a2ce103958eb2443158163dc813d7356`  
		Last Modified: Tue, 24 Feb 2026 19:16:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e98576868f9f3beefe90e537b76f7e1a82463733541937c71270b42c6893d85`  
		Last Modified: Tue, 24 Feb 2026 19:16:42 GMT  
		Size: 13.8 MB (13821714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06881944ca3281956c4a7b7d25ff5b10b8dea392ee0b2efc4d2b1470c1cc524d`  
		Last Modified: Tue, 24 Feb 2026 19:16:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fb6ec216fa16e997804a859784370fda2e6a52f58321654a7ffb190da26b68`  
		Last Modified: Tue, 24 Feb 2026 19:16:42 GMT  
		Size: 13.3 MB (13339431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3f1a329581ad1329731a58f7e06d8a7d84b6bc268bac99d822a050672db30`  
		Last Modified: Tue, 24 Feb 2026 19:16:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d057065cee89fa6f058c140f7a1febfe21a90cf676635e1461190891f5dadcb7`  
		Last Modified: Tue, 24 Feb 2026 19:16:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3446460c54a47bcbb3e80a464820f60cef1d9c25d1830b48dedf597fb92eba`  
		Last Modified: Tue, 24 Feb 2026 19:16:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc846a5f1ed640816f8d9598f80ca9e8da7871fd4edcc7ae85bc4407abbd668`  
		Last Modified: Tue, 24 Feb 2026 19:16:44 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871647474272f8a1ee788cc2cfb4e21ac3bbc3fba7dc616207aa43dc199d0c4b`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 1.6 MB (1591108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e6a66b7b4e867cb676d2eb07fad812b82d340c7ec543cf9db898a5d4a28486`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d516022a4ae325c1ea9be5e7b3a4b47f0b3e97b29c27fafa9cbf485beed65048`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 777.5 KB (777544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7699e025b959d567bf5cbcd9bcd374c37c3fa5c49edb1642ecb9cd1aff787885`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd55d7bb8da85c86a6318892214fc94de08e9a3e4856035a4e114e6ea42a85b`  
		Last Modified: Tue, 24 Feb 2026 20:16:02 GMT  
		Size: 21.3 MB (21309198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:84f0ac330016a82b3f3d75a20b84771cf3d5a3a4562aee24a65f8e1a8e58faaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c23370f622cd1369e549e7f55de42a91d70af352c619c9ed55be3e1579f2ea9`

```dockerfile
```

-	Layers:
	-	`sha256:2c252edd4297605e09e302a6b826352383a8f94a0d88ac541106ad34f65d7632`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 6.9 MB (6908481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1d21873c80448ced59c162f8b943387333f515fe033c7390b6af8c4e4af74e`  
		Last Modified: Tue, 24 Feb 2026 20:16:00 GMT  
		Size: 38.5 KB (38459 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:114bc447b1208659f1d7d26f860c225e0ed241eb928f0dbcdc50e64a8dbe68ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199049975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b08990a17b83a6fdb9c26c481058e365e66b6c3874ab72a7755a4ef0de94ce1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:59:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 18:59:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 18:59:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 18:59:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 18:59:58 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:04:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:04:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:07:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:07:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:07:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:07:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:07:04 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:07:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 19:07:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:07:04 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 19:07:04 GMT
CMD ["php-fpm"]
# Tue, 24 Feb 2026 19:58:05 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:58:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 19:58:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:58:05 GMT
ENV DRUPAL_VERSION=11.3.3
# Tue, 24 Feb 2026 19:58:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Feb 2026 19:58:05 GMT
WORKDIR /opt/drupal
# Tue, 24 Feb 2026 19:58:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 24 Feb 2026 19:58:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1cf78af71ee5fac784620feff9b89b3fc3d9634da6592d1194fc2b920ff2e5`  
		Last Modified: Tue, 24 Feb 2026 19:03:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5db48ef5c27470fb3bdcb3b93e3dcb08709a0faac516f4e026ebdc0d14e48`  
		Last Modified: Tue, 24 Feb 2026 19:03:54 GMT  
		Size: 116.1 MB (116145246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de807c0c3b4d8d9ac2f58103d526bebef9eb0bb86237877fbed903c435a9f50`  
		Last Modified: Tue, 24 Feb 2026 19:03:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129e75569a484100c0c3fe03a178f8fb62625b64a20e21d0152c6883d7cdd65`  
		Last Modified: Tue, 24 Feb 2026 19:07:14 GMT  
		Size: 13.8 MB (13821019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d70cd7a90f0a614f77d847b4c1407e4723e16dfee49cdd988b16ebb6d9feed`  
		Last Modified: Tue, 24 Feb 2026 19:07:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c4b6590840d2db8acf7c309b3c10ffd4b354ff020bdda254fd4052f8140340`  
		Last Modified: Tue, 24 Feb 2026 19:07:14 GMT  
		Size: 14.0 MB (13976527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5a9e9b00f5088249e2d019585ee16b4fcf143112a29e3e8b27adefeb7a109e`  
		Last Modified: Tue, 24 Feb 2026 19:07:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a093d2b001b3f549b1f09cbb991d846d0216c405b2bd8ad9c903c43bf591cb`  
		Last Modified: Tue, 24 Feb 2026 19:07:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13dd4718f80b804f68b6d7728b3b92ec7cb0b812fc4ca9907f3a63c0a801d7`  
		Last Modified: Tue, 24 Feb 2026 19:07:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0996bb622a21fec01cbfe4ec2cdf529c9b6f0eb3173782f125d6a474493262`  
		Last Modified: Tue, 24 Feb 2026 19:07:15 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54db2feb66e6a38d9a6a46ccc1da4a8229e7bd032ed14efb225fcc99e3624fa7`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 1.7 MB (1714220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4e992fc0a1fce3be14b99c07f9b6fc9d021772eff1da4da4dd2bb97aa159fc`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1fa4e1216a2f4b933aad6c337ed8e8530bdc42522ff97d98b0f561c1a51a64`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 777.5 KB (777540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db13628f85a7bed9fe9a89c78683b43b3a1fba2ddf20432327e7422b416790`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7283da849eb80e1298a7b3cdeab5288d8b096a61ba434883880bfe541e398b`  
		Last Modified: Tue, 24 Feb 2026 19:58:30 GMT  
		Size: 21.3 MB (21307891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:8fa9fae96492e7d8ea1d4d7ade830992e2c9f898a11852d8f032174dbb2d5823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba5ca2377c283e117b7cb3a46d1fe4309a0f12f8e5bb4c010aaf0ba67683dff`

```dockerfile
```

-	Layers:
	-	`sha256:36fcd28d24675d02d65612f58a05986a72de6d28742e338dc2a40c297012052c`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 6.8 MB (6784875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5f6e4e2e674bce103db6fcdd403543b93e84f6641ef6f9d601ee5aeaace020`  
		Last Modified: Tue, 24 Feb 2026 19:58:29 GMT  
		Size: 38.1 KB (38052 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:e2d41ea3d50f82526f4fe4c4849726074a54ab49cdacc25d3180e41f2a59ee97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195170781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691aee30092c20db7a7ea464d5d7eb37edff5752be66528322fb35f3fcbb54df`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:47:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 19:29:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:29:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:39:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:39:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:39:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:39:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:39:47 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:39:48 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 19:39:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 19:39:48 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 19:39:48 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 21:19:08 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 21:19:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 21:19:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 21:19:09 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 21:19:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 21:19:09 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 21:19:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 21:19:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5aef540a1dbd10111c40eb7d9fc2480005c3fd8d164979371878603dac2854`  
		Last Modified: Tue, 03 Feb 2026 02:53:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282dc5cdeff5e017f78b0496f224050268f625b87ef7cefd7cdd16e6abf1d723`  
		Last Modified: Tue, 03 Feb 2026 02:53:17 GMT  
		Size: 109.6 MB (109597358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f41d4ecbf32a9e015fc638210e66283419cedac7dd29494bd26c767c870b92`  
		Last Modified: Tue, 03 Feb 2026 02:53:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ac7db65311108a05b46d4b285b61a8bc7d014dc0dce0d7b81407f314e09a7f`  
		Last Modified: Fri, 13 Feb 2026 19:34:25 GMT  
		Size: 13.8 MB (13836950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313df2f165a3d1d101f0d99e8c35d765863cb0d38c8f8f0346c13d271c9a785f`  
		Last Modified: Fri, 13 Feb 2026 19:34:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094294c40a5298bdc6068e1bce48a621e4ce715eb9737127385085ea892aa4e3`  
		Last Modified: Fri, 13 Feb 2026 19:40:15 GMT  
		Size: 14.2 MB (14213074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd9669ad0f759a0594c17b664b94b926b95db6ceda3177760dbc78d5edf6a3`  
		Last Modified: Fri, 13 Feb 2026 19:40:14 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa53fcfc945b127c1080fcc89344c08fa45a625d10c370547ed29e4a62a240`  
		Last Modified: Fri, 13 Feb 2026 19:40:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d1a7c159520f5c37da17cb2ee92cb6467bd2f5c6e20a5a7772ddf949a3f152`  
		Last Modified: Fri, 13 Feb 2026 19:40:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa3e38d3c7ab2ecb1c4caf466da0caf11009cfd76db40cbf31a567d508424b`  
		Last Modified: Fri, 13 Feb 2026 19:40:15 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce531efcce6deb16b2323c69cf1996f54294fb57e66b5439682576ba9178d2e`  
		Last Modified: Fri, 13 Feb 2026 21:20:09 GMT  
		Size: 1.8 MB (1823549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805e8e228c94117ff1c22fc4fd8a6f74c825d8df2bf9b696fb0484d31923f3d3`  
		Last Modified: Fri, 13 Feb 2026 21:20:09 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b398b55052b6a0e231c25efe5db381f6d0f1c180637c4bf626e687991bff1e21`  
		Last Modified: Fri, 13 Feb 2026 21:20:09 GMT  
		Size: 777.5 KB (777547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ebb34ee3ba6529d9aef314241da4dac9f0627d8a978e0815231ebeaa56d806`  
		Last Modified: Fri, 13 Feb 2026 21:20:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4aaaf09640784f996ac672c58d414ae48b4983bc920c9bf360c1516e3380`  
		Last Modified: Fri, 13 Feb 2026 21:20:10 GMT  
		Size: 21.3 MB (21308488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:7673a69b9299dee9fd78883e599cfd63d9e4f09a6580e793bbc5ba88526725c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6849121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d4d7cde22c9f6630f94614f5c5b653c2378588cbc3f699fbc70cfbb002368c`

```dockerfile
```

-	Layers:
	-	`sha256:012ab43eccdb718135764c7b1c356d198331ab706503ba5544b93e4970381c68`  
		Last Modified: Fri, 13 Feb 2026 21:20:09 GMT  
		Size: 6.8 MB (6810836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee39e4bfc3fbefe46fe8461cbb977f12a0c65d3fe627d39f80016c197bb022c`  
		Last Modified: Fri, 13 Feb 2026 21:20:08 GMT  
		Size: 38.3 KB (38285 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:56df1e124285e8cf855a55f804c789010eab0289e36d2a144349c299bd3aaba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225481119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea17b1dd16e49e8ff5923025e43946fc2126ec09167c4e66b480a2e43ac1ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 17:08:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 17:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 17:10:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 17:10:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 17:10:42 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Sat, 14 Feb 2026 05:04:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Feb 2026 05:04:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 07:55:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Feb 2026 07:55:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Feb 2026 07:55:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 14 Feb 2026 07:55:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Feb 2026 07:55:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Feb 2026 07:55:52 GMT
WORKDIR /var/www/html
# Sat, 14 Feb 2026 07:55:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Feb 2026 07:55:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Feb 2026 07:55:52 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Feb 2026 07:55:52 GMT
CMD ["php-fpm"]
# Sun, 15 Feb 2026 09:05:52 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 15 Feb 2026 09:05:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 15 Feb 2026 09:05:53 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sun, 15 Feb 2026 09:05:53 GMT
ENV DRUPAL_VERSION=11.3.3
# Sun, 15 Feb 2026 09:05:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sun, 15 Feb 2026 09:05:53 GMT
WORKDIR /opt/drupal
# Sun, 15 Feb 2026 09:06:35 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sun, 15 Feb 2026 09:06:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0c7bf9985f7aa3278051e22de8b2e25e48b9247e1f8ee94b0580a41f8dbf`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c308411999737082a164f0c80e801b9bba1f870be1efa26fb715f1dd002ad6b0`  
		Last Modified: Tue, 03 Feb 2026 18:14:01 GMT  
		Size: 146.6 MB (146578579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8ed6ff919b7995bbffcb5df8a9d82dfddafe0ad63dc244974287839a83ee2`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9955d80a42c36cbf322ff7692a4f2c02f53aacd9320ee25e0c3d3fa15069700`  
		Last Modified: Sat, 14 Feb 2026 06:02:28 GMT  
		Size: 13.8 MB (13836768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bcd1650379fd3d2ab8e7109924c5b07a773fcfae8655a3b70a2c358b218b12`  
		Last Modified: Sat, 14 Feb 2026 06:02:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803c002eed89bb769e6db69c62f7e5a0f3cfc54873cf1908b5fde506a4b11d65`  
		Last Modified: Sat, 14 Feb 2026 07:58:51 GMT  
		Size: 13.1 MB (13138738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de38907292e23823eea6bd3545e72db85b234dc9f5d5773ebd1fb6215a399277`  
		Last Modified: Sat, 14 Feb 2026 07:58:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea901cf848b515c6364553903564ba6fb4d9700cab440796842828bd56fe794`  
		Last Modified: Sat, 14 Feb 2026 07:58:48 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fafb570451674192c4e8f856e824fe1a244874cefc18d9ee90f30a4436ce3`  
		Last Modified: Sat, 14 Feb 2026 07:58:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72bf61ab2fc36b7437679ea09a130e7203cceb20b25064566163f831fc490fb`  
		Last Modified: Sat, 14 Feb 2026 07:58:50 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4a2add307a8c8966d6d7810f63a7ec12aef162f134427f39c694a348aa2c5e`  
		Last Modified: Sun, 15 Feb 2026 09:11:06 GMT  
		Size: 1.6 MB (1550418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c44b25415bc819be2564adcbb9fc0130b79d2e3e47a4ae472fc54a1b7ef52d`  
		Last Modified: Sun, 15 Feb 2026 09:11:05 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1150ccfc9cbb05ce80223ef959bb1cdb3982b342194c57a20fc3df3dba2ec590`  
		Last Modified: Sun, 15 Feb 2026 09:11:05 GMT  
		Size: 777.5 KB (777547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087cc3187f3914a593493ba482af5953772a8366fa586b86ba28b0e79b8621d1`  
		Last Modified: Sun, 15 Feb 2026 09:11:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922853b899f1e4cc1a4b9d181f8aa68bacc68eca9d17d428465623282de467a2`  
		Last Modified: Sun, 15 Feb 2026 09:11:10 GMT  
		Size: 21.3 MB (21309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:684053ba3f9e080ae9915e6c245de4d1d54bb0eb8c0c7aabc421a6ae78252206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6921182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c665387f8a1bce46ad447401895afae8581d1e74b101171f1010da51ce0c98c8`

```dockerfile
```

-	Layers:
	-	`sha256:6759ef2119dc7a05d52f0f8102ba764d4382b278376d6d93d03a982af8e3e8ed`  
		Last Modified: Sun, 15 Feb 2026 09:11:06 GMT  
		Size: 6.9 MB (6882897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0da86a2795745fbd926bf3bf136515ff4a7c7a0da52fb30e151cb3de5f88fb`  
		Last Modified: Sun, 15 Feb 2026 09:11:05 GMT  
		Size: 38.3 KB (38285 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:1865a5feed2e3f901a03134e41737090df9991a4fd377b491d58dc822421c923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173454375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71dca9e639ab164498c359e92c686df731e228b900fe8f211143e946fceca88`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:26:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:26:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:26:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:26:44 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:52:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:04:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 19:04:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 19:04:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 19:04:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 19:04:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 19:04:02 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 19:04:03 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Feb 2026 19:04:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Feb 2026 19:04:03 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Feb 2026 19:04:03 GMT
CMD ["php-fpm"]
# Fri, 13 Feb 2026 20:14:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 20:14:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Feb 2026 20:14:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:14:09 GMT
ENV DRUPAL_VERSION=11.3.3
# Fri, 13 Feb 2026 20:14:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 13 Feb 2026 20:14:09 GMT
WORKDIR /opt/drupal
# Fri, 13 Feb 2026 20:14:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 13 Feb 2026 20:14:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549210c719d320a22b8bf177acb816a6d0a7f20e7093e59116bfeb44e7274e77`  
		Last Modified: Tue, 03 Feb 2026 02:29:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4813f2bd608dbd0dbe552bceb021d2482736af40cc9da0ca38931df91ac57db`  
		Last Modified: Tue, 03 Feb 2026 02:29:44 GMT  
		Size: 92.6 MB (92567360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda8f1dea52189d07742c4c8d84b6cf3d696d06f26442e2c14c0f3086587f6fb`  
		Last Modified: Tue, 03 Feb 2026 02:29:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d4d1b22437b004b61af3f9a07e43219584ba596e3822c3e44a11d98a5bf2af`  
		Last Modified: Fri, 13 Feb 2026 18:58:15 GMT  
		Size: 13.8 MB (13836079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15efe50d053101bf383708c713ce229933266bb86169752765338edd07763c0b`  
		Last Modified: Fri, 13 Feb 2026 18:58:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835eba3c180ad344641749082c0bee427a5481773cd957cae3db6e85cec928e9`  
		Last Modified: Fri, 13 Feb 2026 19:04:31 GMT  
		Size: 13.5 MB (13460286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b323cfa6cb1387e4f296524a62379f9cb624243bf34461e1be72a64093a425`  
		Last Modified: Fri, 13 Feb 2026 19:04:30 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef1c754c37e5ef582e106fe300600efba6d5d4f0b90efdbaaad51d97d1682c9`  
		Last Modified: Fri, 13 Feb 2026 19:04:30 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d85414540ade0f97d907c802a59e650052e11884da2d4fd1627b3b124934fe`  
		Last Modified: Fri, 13 Feb 2026 19:04:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7aa7dc3d384a686843fcb9b79cb4c74c82b600d4d4db5ba9188ec49ed15818`  
		Last Modified: Fri, 13 Feb 2026 19:04:31 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c5e868cda460345d7d5f92c6161902eaaf1ac8a8cb0c98de26b0cec1b70c44`  
		Last Modified: Fri, 13 Feb 2026 20:14:38 GMT  
		Size: 1.7 MB (1652273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac0beb3dd23dee92e24d9828c817b8829db18c1c5a1321ad3a195ed9f94182`  
		Last Modified: Fri, 13 Feb 2026 20:14:38 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861ee040e000d3f8eb086d3b78d593e7d36244731f9e1f7508afef271a7b22d`  
		Last Modified: Fri, 13 Feb 2026 20:14:38 GMT  
		Size: 777.5 KB (777535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f0db07207d5aa48955a04286c3bfec3d2d090aa56de1bfe88202b11cedceb2`  
		Last Modified: Fri, 13 Feb 2026 20:14:38 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495eeca0676782a8e97c83a92a7db734e1bb7bc9dc9dc268f141ebbc5153fd80`  
		Last Modified: Fri, 13 Feb 2026 20:14:40 GMT  
		Size: 21.3 MB (21309066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:be72745c11efb20556f59837149ecb36eb253ae7c4738ee75d563726fd5112b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60db560fd14c7a1877ef1308645d791a0706805c5b46cc9092109fef1e9bc7d`

```dockerfile
```

-	Layers:
	-	`sha256:ca723649f7980f977e9969b55ab24b607f79495925c88a7d22c9d427c6312653`  
		Last Modified: Fri, 13 Feb 2026 20:14:39 GMT  
		Size: 6.6 MB (6628317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e1f4d0afdd5a3c055883b00887fff580c263cd43f9cf3bb701c370712419b7`  
		Last Modified: Fri, 13 Feb 2026 20:14:38 GMT  
		Size: 38.1 KB (38149 bytes)  
		MIME: application/vnd.in-toto+json
