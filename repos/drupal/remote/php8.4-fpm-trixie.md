## `drupal:php8.4-fpm-trixie`

```console
$ docker pull drupal@sha256:a4b3de03f56171e24b327e098aab0929edcc84edfbe160f60d223f6d3bb804c1
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

### `drupal:php8.4-fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:9895d892db9ad49584803105b9649b9c0a56f20ab7abda867ef0a90c3026c1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198812100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d381bf9706476810feac0e1da2a3298c575c6a789b59f2fbaa745ae3659f42f1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:23:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:24:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:24:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:24:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:24:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_VERSION=8.4.16
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 13 Jan 2026 01:24:01 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 13 Jan 2026 01:33:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:33:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:36:03 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:36:03 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:36:03 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:36:03 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:36:03 GMT
CMD ["php-fpm"]
# Tue, 13 Jan 2026 03:53:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:53:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:53:48 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 03:53:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 03:53:48 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 03:53:56 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 03:53:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224621b58e9b733bd8c865aad420c4267c783c7761e93fcfc03dd694d302290e`  
		Last Modified: Tue, 13 Jan 2026 01:27:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f23dabc7d3f3a37cef5d4b78d5ddb72cf59db10d688d58698a27c9561ae730`  
		Last Modified: Tue, 13 Jan 2026 01:28:01 GMT  
		Size: 117.8 MB (117839779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37263e7f1bed31848037cc115eb2e791158b48c887f623b759a6fbde505fc5cd`  
		Last Modified: Tue, 13 Jan 2026 01:27:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec24a4ab0a8e487d4cbf12080c9542c5cf9ea1000f2a34540049aef7ac2ac388`  
		Last Modified: Tue, 13 Jan 2026 01:36:32 GMT  
		Size: 13.8 MB (13808467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a1edae25a8508732db8e4cb9880d1af125fa32519d827a1c0a2e7f2d422f1`  
		Last Modified: Tue, 13 Jan 2026 01:36:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b83f53fc1677834945ba244a0c9cf97cf23be48364ef0cd638715e142d2672`  
		Last Modified: Tue, 13 Jan 2026 01:36:22 GMT  
		Size: 13.7 MB (13666086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608d0f562533f736ccfae70684b01987a396a3712627dc684aaa1690c746aefe`  
		Last Modified: Tue, 13 Jan 2026 01:36:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7afeda9ad606d16c88e37cb879ad74a6352a69dbf5afbde5a99f087d86342dc`  
		Last Modified: Tue, 13 Jan 2026 01:36:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bff3fdefc1915324e11fea690f50de4dbc9e091f15b67af875ece09151af57b`  
		Last Modified: Tue, 13 Jan 2026 01:36:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d153956301a89acdf88d2e65c8871fc1b04fbbc7bedcb64342c26356ce99e6a`  
		Last Modified: Tue, 13 Jan 2026 01:36:21 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d982cbf0646310568ee032a3992b80b3d18fa76ae31801eddbb97cca8cbb4`  
		Last Modified: Tue, 13 Jan 2026 03:54:20 GMT  
		Size: 1.6 MB (1634232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7042057e112c27c04f7471133be03f6c37fe82c873eed6c939b2a030b3053ace`  
		Last Modified: Tue, 13 Jan 2026 03:54:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7b01312a840007c280f0173d4301ad2129470afb5be21e31db165b51ccea22`  
		Last Modified: Tue, 13 Jan 2026 03:54:20 GMT  
		Size: 776.4 KB (776358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7d0c63c78df0ee0e9e919c4f152a4c1ef68c0711a21efb48d2bd6da0be334c`  
		Last Modified: Tue, 13 Jan 2026 03:54:20 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b252d274fabe9102933bbac20d4d1f71d02b9a6c9e0ccd9a36fe8fd8776e5`  
		Last Modified: Tue, 13 Jan 2026 03:54:21 GMT  
		Size: 21.3 MB (21299949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:3502b65a0115677a9fc8769b0108e7bada2f76fe00b841ba79294f3874c1b122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6849206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6493abba44eebf3cdfee6ba0232e877235f99a5f205e995f83cdd1f20b05dcd5`

```dockerfile
```

-	Layers:
	-	`sha256:c600616161c7196703a93484cb8e833d63bdc5b73a8e0873ec335f8b53b0381b`  
		Last Modified: Tue, 13 Jan 2026 06:07:28 GMT  
		Size: 6.8 MB (6811051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58a449fe4212f429ed1dfacab78921b67720bf40852e62dad8f9ddc9708374f`  
		Last Modified: Tue, 13 Jan 2026 06:07:28 GMT  
		Size: 38.2 KB (38155 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a032b92a3c44e73cac899457e5529e6df04c7217be76eaf72090f9ebb4994de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161257780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14d5ece116edb29156943c30837b2bf5132e43793ec76905133f3a45c047cb4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:29:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:29:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:29:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_VERSION=8.4.16
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 13 Jan 2026 01:29:38 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 13 Jan 2026 01:51:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:51:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:54:37 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:54:37 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:54:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:54:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:54:37 GMT
CMD ["php-fpm"]
# Tue, 13 Jan 2026 04:27:04 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:27:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 04:27:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 04:27:04 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 04:27:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 04:27:04 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 04:27:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 04:27:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4415bd043f40b57f82da9967544e4ecc0806ab76cdca6d902cf50fe18b9f6e04`  
		Last Modified: Tue, 13 Jan 2026 01:33:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c148fd3910de1c70c5b50cf11648ed2a4efa85de180b3e863180e34b9bce074`  
		Last Modified: Tue, 13 Jan 2026 01:33:36 GMT  
		Size: 86.2 MB (86244682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cd76bdbba1cfd183d5e51b921a93d115ee1e3e8575952ea9b0aa2e71f381eb`  
		Last Modified: Tue, 13 Jan 2026 01:33:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c4b6d55196d76e693c3ec0826ba8296069f67f6415627b6a8e9cf350c305f4`  
		Last Modified: Tue, 13 Jan 2026 01:54:55 GMT  
		Size: 13.8 MB (13806401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67ecff5e25bde5167d8e17db0626b0f060d9013956bcbd8f6ce9da407c84fbb`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25215a2df3007a16619fe4774bd453e2d62c787078710ef3e06bf5dea0c5b239`  
		Last Modified: Tue, 13 Jan 2026 01:54:55 GMT  
		Size: 11.6 MB (11560596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea2fb14195afb17ea804975303689955db7d8c9c4cac2190d1018248c6485a`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a68c8f6167e30d969ebbe06d71d8444a1813badd136d4df0a4d859f1ce1ce1`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e88e16b1e1510d30bb52fbaf67afc28b4ef37c11b021cc6f75ae347f7f3c8`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e40a598bcd06f7bf560632a9cf29f5fd787427d590ac0ed48562b644dc428`  
		Last Modified: Tue, 13 Jan 2026 01:54:54 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d7ac2158bce4f8766882a5d084a71f6c673614a3ac84094f5b79688ae4f58`  
		Last Modified: Tue, 13 Jan 2026 04:27:35 GMT  
		Size: 1.3 MB (1347471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5500fd2633e42aa52ec2edc066877257b21eb3ae37f343384bd3f2995d0e8595`  
		Last Modified: Tue, 13 Jan 2026 04:27:35 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc39fe8c369bc970db2b84014ed7971e89e1b6bcdae4b26703baa09889605cec`  
		Last Modified: Tue, 13 Jan 2026 04:27:35 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f6a8b4559796c86516c0f14f767a7140ef7cf2013e4b59abce8fffd77916b2`  
		Last Modified: Tue, 13 Jan 2026 04:27:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646cd9b9f1ccb0f363c14c2e517ed29c587001990a0aacacb8fa6f9d23668f20`  
		Last Modified: Tue, 13 Jan 2026 04:27:36 GMT  
		Size: 21.3 MB (21300150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:27e7b61b69a1c3fa2cb15822c4e989883a1a0cb56b87535b8b8992c758860e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6653319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ef4821b65882553d7727cdbd8815aadddd6bb193ce737bea22d7037d8f825`

```dockerfile
```

-	Layers:
	-	`sha256:5d390da17daf206fafbbcfec9b9e2e4d61fd0f12c1e2c259759bd290efdcd3f7`  
		Last Modified: Tue, 13 Jan 2026 06:07:35 GMT  
		Size: 6.6 MB (6614948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77d9a9c2bccfe3c3a3810acc22158bd11431fd1437dc72360e4e4f5c8f630f1`  
		Last Modified: Tue, 13 Jan 2026 06:07:36 GMT  
		Size: 38.4 KB (38371 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:a6e22d243cb0c310afcf7300b6dc74a67a751243b60dcc005a69e87ddb3eb663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191122496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a943044ee2e010a22f21ad1e5f0bab96d547392ee9f993bc3e64db66e4f1e719`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:23:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:23:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:23:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_VERSION=8.4.16
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 13 Jan 2026 01:23:52 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 13 Jan 2026 01:33:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:33:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:36:32 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:36:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:36:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:36:32 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:36:32 GMT
CMD ["php-fpm"]
# Tue, 13 Jan 2026 04:00:07 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:00:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 04:00:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 04:00:07 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 04:00:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 04:00:07 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 04:00:15 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 04:00:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38952fa31127bc40ef3203cfe782a6f0166c149e544f1d08619d799e3b258f`  
		Last Modified: Tue, 13 Jan 2026 01:27:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d8fc19f1ccc97709797b782c96fd4659339060b8d27f0ece159f4da4419e9`  
		Last Modified: Tue, 13 Jan 2026 01:28:13 GMT  
		Size: 110.2 MB (110164285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529106ca5ed23c98dd76ffb22f13dcfe44b44ccfb20c09c510966ad2e37f80aa`  
		Last Modified: Tue, 13 Jan 2026 01:27:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec74e998995b4c68aa5a65df7e1591214de4ca9b20fa9effb85602103f85d1fc`  
		Last Modified: Tue, 13 Jan 2026 01:36:52 GMT  
		Size: 13.8 MB (13808094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48110138ce0bdc66f8317e1a25ff07c77e0051841f1ccd172d339f0558ad7faa`  
		Last Modified: Tue, 13 Jan 2026 01:36:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4328e7f564d52fde4cf6610cefbe8193d1360161d9ef3fd1b6981a0dd11a345`  
		Last Modified: Tue, 13 Jan 2026 01:36:52 GMT  
		Size: 13.3 MB (13334965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c6d3aaea6815d1b81753cfe20028d3aeffaa47f1da80fb809afa04870fc333`  
		Last Modified: Tue, 13 Jan 2026 01:36:50 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3fc5cdc702b8e4022d8aaab1128eb82baaea3546e820d8bbcb8d20746a067`  
		Last Modified: Tue, 13 Jan 2026 01:36:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba5f032e66adb827e8bd5bd6737c3dc158e6ee81f93e0488cf5ed09f06a3d5`  
		Last Modified: Tue, 13 Jan 2026 01:36:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739cb6fb03a4e531303f6888036944485c976d9096a54c090250a75716ba0e3`  
		Last Modified: Tue, 13 Jan 2026 01:36:50 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2019117a72f93d949dee1e414a9b07a30bb54917f0ee37d74e6ff8178198cc3`  
		Last Modified: Tue, 13 Jan 2026 04:00:45 GMT  
		Size: 1.6 MB (1591332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05327252c27c0c990369cbe60a74c236c89f2f1a35ab069ebf768c6c605fcc5b`  
		Last Modified: Tue, 13 Jan 2026 04:00:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f429ce69736cedfdf4e884742d03c38d2c9b6ec35b089f2ce206b8c41af4360`  
		Last Modified: Tue, 13 Jan 2026 04:00:45 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbab96b32bb53b6b0356a1f30278dd0e367d96693ec0f8d593248ff3ba58049`  
		Last Modified: Tue, 13 Jan 2026 04:00:45 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fb388d24d5504489eda09ec63c61e0c5692f97bb00a063f4bac145c57ef7e7`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 21.3 MB (21299879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:7b9bd6bd1f931845edb35eca776898b4972e4aa46e8742e33a19c12b16f155fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29ce2b27c748d06748216f59754391bb29be0d3e39b9c169ace3313ea2824bd`

```dockerfile
```

-	Layers:
	-	`sha256:43aa3a57404aaa1f488a75d1258e8e83c408a9e9aa650c1dd4c92fef2abbafb2`  
		Last Modified: Tue, 13 Jan 2026 06:07:57 GMT  
		Size: 6.9 MB (6908481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213b93e4c153dd225224a62ce4556c58bb25fed1cdefae93b6442ff91952506d`  
		Last Modified: Tue, 13 Jan 2026 06:07:58 GMT  
		Size: 38.5 KB (38459 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:c9c8f83023b589e904e1b1412337c679831db600ec05e27da2e9ed72623228ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (198997563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc769c36134f77192db6332c7b87d81c44c3e81cbd65d4f949e9df92fcef1952`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:28:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:28:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:28:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:28:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_VERSION=8.4.16
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 13 Jan 2026 01:28:03 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 13 Jan 2026 01:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:35:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:35:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:35:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:35:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:35:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:35:50 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:35:50 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:35:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:35:50 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:35:50 GMT
CMD ["php-fpm"]
# Tue, 13 Jan 2026 03:07:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:07:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:07:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:07:41 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 03:07:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 03:07:41 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 03:07:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 03:07:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c770992f029624e5f0f0ef2e5018f2b3f8b115740a4f9d1f55829f7804499099`  
		Last Modified: Tue, 13 Jan 2026 01:31:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f96b9fc99af1fd52cfe759a06329795087cd32d385c70f9982e56846b1f1d`  
		Last Modified: Tue, 13 Jan 2026 01:32:10 GMT  
		Size: 116.1 MB (116139059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7474ebe1a55cb2e63de18cdd2bd2bbcb342ea44f771c40fe6ee9b8002c639e9`  
		Last Modified: Tue, 13 Jan 2026 01:31:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b690f3241382b0c586ceaeeacd39423d8e9b42677471d64a42b80dd26504020`  
		Last Modified: Tue, 13 Jan 2026 01:36:09 GMT  
		Size: 13.8 MB (13807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37e74074394595eb87b11e76b5f0e4d408410354d900dce85c886a29e328e0`  
		Last Modified: Tue, 13 Jan 2026 01:36:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff1fc6660a14a205141cee2beeaccc45d3e1c30d4f5fdd87c3f9b215b85c3d`  
		Last Modified: Tue, 13 Jan 2026 01:36:09 GMT  
		Size: 14.0 MB (13958306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3927671997ae5b5fe9321a67e694a4229788426b9eed8d65fb76b4a950de76d`  
		Last Modified: Tue, 13 Jan 2026 01:36:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7ce3fcf073699862c1ce73f04a53b1fd744c8949e29d38ea099352d25a3f2`  
		Last Modified: Tue, 13 Jan 2026 01:36:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c892cf8cd5d784e5c4cf7b6a6a9be211721bc5577a48d0583e367d60afc40c1`  
		Last Modified: Tue, 13 Jan 2026 01:36:08 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463bdcadd45842bef7793379861537a7bee1b4b699142817018ea90debffca7c`  
		Last Modified: Tue, 13 Jan 2026 01:36:07 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5672efb6fdb5aff623e11057cec50538b8c14f1df75a5541e22833f6cac0d934`  
		Last Modified: Tue, 13 Jan 2026 03:08:12 GMT  
		Size: 1.7 MB (1714261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e79e69210af8cc867b9848b1b9352e18d717d5ec6295653ca3afa6367f2e87`  
		Last Modified: Tue, 13 Jan 2026 03:08:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6263af3c25cb32cb3bc345bcd765e45aaf77c5275f60ac46f89aeaa7a1d44327`  
		Last Modified: Tue, 13 Jan 2026 03:08:12 GMT  
		Size: 776.4 KB (776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239ad2ec098c20c19a13fa2cafd3d8d5cf8574abe0f67cabdd59331a0771c86c`  
		Last Modified: Tue, 13 Jan 2026 03:08:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fff077215bb51a235dd403424f21ff72de23bab0c977bb4349ab432677df6e9`  
		Last Modified: Tue, 13 Jan 2026 03:08:13 GMT  
		Size: 21.3 MB (21299996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:0d95c0710ab965aabf1cea4d4082b1eecae3b3e81ce7a35477a46c2bd4468f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4994403591519daebbc92d09248b60d533abcb640075005df3c893d606bb73`

```dockerfile
```

-	Layers:
	-	`sha256:30991cdc6958fbb27aac933eba467616a0a57b51bfa551ea406d794f98a1cdff`  
		Last Modified: Tue, 13 Jan 2026 06:08:05 GMT  
		Size: 6.8 MB (6784875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894ada0943befeec7bfd2085a5db16cd8b4af0e430a001b0060b53d54e681220`  
		Last Modified: Tue, 13 Jan 2026 06:08:05 GMT  
		Size: 38.1 KB (38052 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:3565d4f4d784a431ce46caf905a14c1489aa233b45456b47105c6877cc74e43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195140156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef8e2e69781f4d6b318dfc281450bd77a7fa9110b47be5473d13f86a6512fb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 16:33:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 16:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 16:34:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 16:34:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_VERSION=8.4.16
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 30 Dec 2025 16:49:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 16:49:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:22:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:22:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 00:22:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:22:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:22:11 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:22:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 00:22:11 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 00:22:11 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 00:22:11 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 04:34:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 04:34:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 10 Jan 2026 04:34:40 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:34:40 GMT
ENV DRUPAL_VERSION=11.3.2
# Sat, 10 Jan 2026 04:34:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 04:34:40 GMT
WORKDIR /opt/drupal
# Sat, 10 Jan 2026 04:34:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 04:34:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f57655a18e58caec8202718b81878a0a323ee7dc860ee03487665b00f17d4`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8947d9b26fd5842181dbfa0476ae87283eb4ee0896468eef4401a617eae0fb`  
		Last Modified: Tue, 30 Dec 2025 16:39:26 GMT  
		Size: 109.6 MB (109598066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0082faf6428f6d353e1b13563b033f41260118184f280753196d05c13071880e`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc8905e3e20ca9fdada53e03c62be38397b183802e00f36e9fdb8ba80156d67`  
		Last Modified: Tue, 30 Dec 2025 16:53:06 GMT  
		Size: 13.8 MB (13807682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07be3ddfc6042d71149b308d776543d00c04d4c98d32adb199421371a5d9ec`  
		Last Modified: Tue, 30 Dec 2025 16:53:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1977b99102b10a700efd16e3b6940036142f8f3e12e77ab5893b078015dccf7`  
		Last Modified: Sat, 10 Jan 2026 00:22:50 GMT  
		Size: 14.2 MB (14225302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794eb907e0753dbf1e17084839e04159f1317f0b302f748d772b8f7ec06b96e7`  
		Last Modified: Sat, 10 Jan 2026 00:22:48 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ff938b8cb0e749f6156d27805313cff3e7d7d59587ac8be43d771fc0af34c`  
		Last Modified: Sat, 10 Jan 2026 00:22:48 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208d367d8cbdf33147ecd62aef86b24e7caf72602ab2b97a80503f5ad5608ccb`  
		Last Modified: Sat, 10 Jan 2026 00:22:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c4c5b6bdb576d33b647aa315e421922608fbdc0406a3b84f5c611d36def580`  
		Last Modified: Sat, 10 Jan 2026 00:22:48 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae7a961f4043a5a481faaf8f4e1daa8b3c9b47959dbcf43d750e18ae28ca531`  
		Last Modified: Sat, 10 Jan 2026 04:35:46 GMT  
		Size: 1.8 MB (1822653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8e97d305efbd11b37f72e05f7d1f4d38519d5f5ef77209dbabc945f89a663b`  
		Last Modified: Sat, 10 Jan 2026 04:35:46 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd78053ad46345c4827c6db43e77657d8bbcd3caee4069ed6c12bc95be52d7f`  
		Last Modified: Sat, 10 Jan 2026 04:35:46 GMT  
		Size: 776.4 KB (776366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3220b0c982b532e5953b6238b549cf335140e3e1ab66b052e1495b9a29931d75`  
		Last Modified: Sat, 10 Jan 2026 04:35:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5070a05b5ff11ea639be74897507341f88787ce97ed31054023fbc85fa450ab6`  
		Last Modified: Sat, 10 Jan 2026 04:35:48 GMT  
		Size: 21.3 MB (21299643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:71089c8a50da58f36b1b2b0f7ddef1f77ee1845855bfcf212b508bb22be9e64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6848987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb68aaefa50ab219c2cf347bc2498306be8840d08cb37151ff01675ccdd2df98`

```dockerfile
```

-	Layers:
	-	`sha256:11a8275c20b5bbc5ffa9e698b64ab210b385f7a2840f934bff217db874ad22c5`  
		Last Modified: Sat, 10 Jan 2026 05:56:48 GMT  
		Size: 6.8 MB (6810702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361da6063dcc70d8098b80b94fe543ea9a2588749958676ce196c05d752bc2e9`  
		Last Modified: Sat, 10 Jan 2026 05:57:31 GMT  
		Size: 38.3 KB (38285 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:0240c1d9aa0fc9142918f0da119f2bd5e56c89a23be9fcd4cc7a705566f756a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225449651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ced4095941ad169a86a68dac2c4aa9d44a9d3551ffc71ca58eef7e9313828a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:15:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 08:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 08:17:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 08:17:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_VERSION=8.4.16
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 30 Dec 2025 12:29:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 12:29:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 15:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 30 Dec 2025 15:20:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 15:20:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 30 Dec 2025 15:20:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 30 Dec 2025 15:20:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Dec 2025 15:20:33 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 15:20:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 30 Dec 2025 15:20:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 15:20:34 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 30 Dec 2025 15:20:34 GMT
CMD ["php-fpm"]
# Thu, 01 Jan 2026 13:03:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Jan 2026 13:03:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 05 Jan 2026 09:53:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 05 Jan 2026 09:53:20 GMT
ENV DRUPAL_VERSION=11.3.2
# Mon, 05 Jan 2026 09:53:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 05 Jan 2026 09:53:20 GMT
WORKDIR /opt/drupal
# Thu, 08 Jan 2026 21:05:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Jan 2026 21:05:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44b1edad4acbdf2eb79bc4ed79ff402d6af38c94857a826c4e8f406f68b8b4`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a8c50b15f754f42cc587a4d423f958f4de65b8cc8da75adfbac833ca87e54`  
		Last Modified: Tue, 30 Dec 2025 11:32:37 GMT  
		Size: 146.6 MB (146578538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346525b0d45631b779c99bb99caa2632c2822ec686a160c5f4d23f9cfac4217`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eff761120826b0f66ef0a13fe85745cc6bf0c30d7eba7c55f22ef609a677d5b`  
		Last Modified: Tue, 30 Dec 2025 13:26:36 GMT  
		Size: 13.8 MB (13816481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd11effed05eec263c43b760416c748f6aee11444cdfc5c4f0438fe7ce41bcb`  
		Last Modified: Tue, 30 Dec 2025 13:26:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d70bf3f90f750dbf1c3e22b0905fd1d911048f840107433aceaf08042a60bf1`  
		Last Modified: Tue, 30 Dec 2025 15:23:42 GMT  
		Size: 13.1 MB (13142370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cca63debdaf23336709f2f12dce1320e74c0b613eb86360722b3e679704d8b7`  
		Last Modified: Tue, 30 Dec 2025 15:23:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df83c881620d9b0eccf81786ee5e833b406a305336b53553d64cb1eb0f1a48c`  
		Last Modified: Tue, 30 Dec 2025 15:23:39 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724057dcf8306e71e224b08ca828198fefa80babe79b8837cce759978286a8e`  
		Last Modified: Tue, 30 Dec 2025 15:23:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731d391483efe20058bf1b0048ccac1e2230df634a5fb6699a2309d7f951975`  
		Last Modified: Tue, 30 Dec 2025 15:23:39 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f46cd4b59ea9cf167769ef7b0e8c1f6aa64660d686734d16370150d79cafa0a`  
		Last Modified: Thu, 01 Jan 2026 13:09:04 GMT  
		Size: 1.5 MB (1549340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8682ed128995cfb06300a75149d2ff8c14b01f48854aaf263391138d2ae14`  
		Last Modified: Thu, 01 Jan 2026 13:09:04 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef25526aac90317eabf82390bb1fb8bcda757fcd636f0ef524a45dc09c789e`  
		Last Modified: Mon, 05 Jan 2026 09:58:53 GMT  
		Size: 776.4 KB (776359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c364cf293ba23e5f897d5efcf6beefd52ed6e1caf5c6dcf8b03bb47b9f04b`  
		Last Modified: Mon, 05 Jan 2026 09:58:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6132091855bfa9cf1dedd30e04d03fc8653e91274c053abdecdc2a8026b32060`  
		Last Modified: Thu, 08 Jan 2026 21:10:32 GMT  
		Size: 21.3 MB (21299883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:cbfa9d02dd400ee4e5801bb733d44e3a62c9647f74e5175ee9a184d36bff1825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6921020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28df0dfc7bef2aaa53c1a1e1e9084cda6e0e4572738e84b2d5aa4c58972c0510`

```dockerfile
```

-	Layers:
	-	`sha256:186d2718874ad01ee8a9a87bfde30620d63cfab9cc58f7d20bc82941be26189a`  
		Last Modified: Fri, 09 Jan 2026 00:07:34 GMT  
		Size: 6.9 MB (6882735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9dfda21bc5087d3904076f876a3599158f89b1e7d3e1196c4f6b735898a58cb`  
		Last Modified: Fri, 09 Jan 2026 00:07:35 GMT  
		Size: 38.3 KB (38285 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:c8a67be6a7ae762194555384c079f92cd6ae0ff1d6f8ee49343b713cc82b963c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173423733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f63a114e570644b345ec1ac7c7e492166a0c9312f5a0b56392c287eea94e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:21:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:21:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_VERSION=8.4.16
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Mon, 29 Dec 2025 23:21:48 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Mon, 29 Dec 2025 23:32:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:32:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:26:48 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:26:48 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 23:26:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 23:26:48 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 23:26:48 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 01:19:04 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 01:19:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 10 Jan 2026 01:19:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:19:04 GMT
ENV DRUPAL_VERSION=11.3.2
# Sat, 10 Jan 2026 01:19:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 01:19:04 GMT
WORKDIR /opt/drupal
# Sat, 10 Jan 2026 01:19:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 01:19:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda3e5b0a481f510e5d340cc00228a59c091a2c65bb4f12fb9345bf33b5b030b`  
		Last Modified: Mon, 29 Dec 2025 23:26:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866e04396dc2365f827282bb5a6974a15c99aa9e068f66c872f5af90cd1f95d9`  
		Last Modified: Mon, 29 Dec 2025 23:26:43 GMT  
		Size: 92.6 MB (92564307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855d1223180ff8f77ca73a479af1a438dc36f7efb7b6c0c6fc4d8aefebc6aa9f`  
		Last Modified: Mon, 29 Dec 2025 23:26:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6908844ae4dd8a20bcb8694cc0e48f46c2addce6338ee483370d24be08591f`  
		Last Modified: Mon, 29 Dec 2025 23:36:59 GMT  
		Size: 13.8 MB (13806983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268390ce58892f957605c63f23d65764912772d99e882ee581c2fee5ec2beca`  
		Last Modified: Mon, 29 Dec 2025 23:36:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e032c8ca243b2a5398b1bdd7b48901c607eeee728e5555721b955801c37cc`  
		Last Modified: Fri, 09 Jan 2026 23:27:13 GMT  
		Size: 13.5 MB (13476111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dbd1506b0340a439580e7e72206345ce762153ea8ffe3f1898c2be0806c6a5`  
		Last Modified: Fri, 09 Jan 2026 23:27:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51692c17f5d7a85dbe97cb284eeb213baf493ceedf5249fc3a34e0585ba47f7`  
		Last Modified: Fri, 09 Jan 2026 23:27:12 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7049d7d6fe46c1c1ba190845209ee26c1078922ccb50f848e254774cce1e689`  
		Last Modified: Fri, 09 Jan 2026 23:27:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0a9acbe1f29eaa1f1ef4465e341ff5c70155afaf17bf2eafba9b854bc4128`  
		Last Modified: Fri, 09 Jan 2026 23:27:12 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ffb38404bf706cc42b475b5e6cb80139b825673dba26963d9c89ed5273668`  
		Last Modified: Sat, 10 Jan 2026 01:19:45 GMT  
		Size: 1.7 MB (1651944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310274722b61f855f856797d8094e777c929c35964b16e8af33b7de348c68e4`  
		Last Modified: Sat, 10 Jan 2026 01:19:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e447249b5d8da62162a4cbf0d8aab5f4b0135088e4c6b829dd2aaeca9a637da`  
		Last Modified: Sat, 10 Jan 2026 01:19:45 GMT  
		Size: 776.4 KB (776366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a936587e4b28a87b29408469d16362573b8bebe4cafb198960a6e816285daa58`  
		Last Modified: Sat, 10 Jan 2026 01:19:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a4f74ccb4abdef2dd3604c3c6998dd85b453b038fe04128997c02c1c63f8f`  
		Last Modified: Sat, 10 Jan 2026 01:19:47 GMT  
		Size: 21.3 MB (21300053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:ee230c5b09a997d6088945aaffab0d26ec30b9b52506d8efcc2c68e0f393b6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6c9fea8a911889e5cb147027b64ea7f4270eeae11797491b7ed729c5ce9d8d`

```dockerfile
```

-	Layers:
	-	`sha256:afce0e4d77bfaf3b1a1ee6345c349ce75c4ae56fb624b8435086764ad76b9e33`  
		Last Modified: Sat, 10 Jan 2026 03:12:11 GMT  
		Size: 6.6 MB (6628183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3dbef88d1a2ea36a7d97a67b394523d0b28799e7de250889ce80aed47b0ac4`  
		Last Modified: Sat, 10 Jan 2026 03:12:11 GMT  
		Size: 38.1 KB (38149 bytes)  
		MIME: application/vnd.in-toto+json
