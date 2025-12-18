## `drupal:10-fpm-bookworm`

```console
$ docker pull drupal@sha256:14fd183a029bd1a806ed5b10ab03f1bc79c1b884ae5c2eee684bf5e0b36a524d
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
$ docker pull drupal@sha256:fd4591ed98a16fd8f76e11667374eb0c82b9dcd4f031029327c88213db5364d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200132657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb8f279ea92649b3489122a34eab8bf17d363599f045caaf5bc014f9fc68b24`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:46:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:46:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:46:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:46:33 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:50:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:50:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:52:47 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:52:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Dec 2025 22:52:47 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:52:47 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Dec 2025 22:52:47 GMT
CMD ["php-fpm"]
# Wed, 17 Dec 2025 23:31:52 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:31:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:31:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:31:52 GMT
ENV DRUPAL_VERSION=10.6.0
# Wed, 17 Dec 2025 23:31:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:31:52 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:34:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:34:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0affb3e83fbe72a795e78bf3653ae856e49ad26cc6fe1c16a1615d9778bf2779`  
		Last Modified: Mon, 08 Dec 2025 22:49:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee66c3c2460ec7ceeb84a8de76edd83a6cc7d7017851f5ed397da10cced238b`  
		Last Modified: Mon, 08 Dec 2025 22:49:47 GMT  
		Size: 104.3 MB (104330668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58ddce05918557e56a37e050bdb1f92c679f1d26ba097c3316e70dc808545f`  
		Last Modified: Mon, 08 Dec 2025 22:49:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b843e650e1cfca4610aace8499f640165449e4ec8e2009db57596113cbd2c`  
		Last Modified: Mon, 08 Dec 2025 22:53:08 GMT  
		Size: 13.8 MB (13762732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505d6eb8e223d3ad129cef26c601fe0f2c4ea96a6b7616704cb154b498957751`  
		Last Modified: Mon, 08 Dec 2025 22:53:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397efcbdf28f35e9b5cc04b653adb668495d14ff2781c5b0d6daf14b1cdd23d4`  
		Last Modified: Mon, 08 Dec 2025 22:53:10 GMT  
		Size: 29.6 MB (29614630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a786d72fcf97310b97178c2686374109242171721359a35b7ec4dd75fa413e`  
		Last Modified: Mon, 08 Dec 2025 22:53:06 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f85f258198420eeaf9f4581eade4d66b9ccd6b4ac5d7928f854c926f898716a`  
		Last Modified: Mon, 08 Dec 2025 22:53:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb8d96ff85693022e7d7394605b2aa360eaa5cd304113a19b3ee9128e15ba67`  
		Last Modified: Mon, 08 Dec 2025 22:53:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9156df08ab1a863c6912722f9bcf0caaa090d30ef30627500ac92ccfff43727`  
		Last Modified: Mon, 08 Dec 2025 22:53:07 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a80568b727aa4eea08b1be6f4075bc06e5dfc89cb76cbd5daa1556a0bb8c0`  
		Last Modified: Wed, 17 Dec 2025 23:32:22 GMT  
		Size: 1.6 MB (1551089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13994168d6de509c240b8ced8df2187533838bd08a66eb62d8476a3a8cd86080`  
		Last Modified: Wed, 17 Dec 2025 23:32:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17f305edcdfd98669feb39acaca5d4b9dfdc30b18b1b4f8819b13ef7643448e`  
		Last Modified: Wed, 17 Dec 2025 23:32:22 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc72c8a6d2062dde81041bb5271a4f51817b161ad5f7d09939732c7761f2a4e`  
		Last Modified: Wed, 17 Dec 2025 23:32:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7dfe52a9c170e97970077a1955a5e4d2eb02226a1cb3edbf3f6209b61a2cde`  
		Last Modified: Wed, 17 Dec 2025 23:35:16 GMT  
		Size: 21.9 MB (21853582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:8852a86dc4b2046690101ee720f92f5b6dcbcc3b1c85fdf33246d7b8bf2456ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb03370ca4dabcc77e88a09d298b45895b3de2347d162448930b2a39d5ee387`

```dockerfile
```

-	Layers:
	-	`sha256:a495b7827bfed1d08f30ce40e45b65c5b2e6952b1a0b054b6b1a6fb86e9e77bf`  
		Last Modified: Wed, 17 Dec 2025 23:56:55 GMT  
		Size: 6.5 MB (6515456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd99498280f2d6903b3fe5ac5f5be56f4e99f9c55bdd7afd11092ff38a4296fb`  
		Last Modified: Wed, 17 Dec 2025 23:56:56 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d998bb766ec09f6875b19156dbf028bc5335da33d00d122101341fba7a4d1465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164665574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705c7a2de544a1d619bfedf0ef0bf8c4845656cda745f0ab59405c711d969f9a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:52:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:52:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:52:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:52:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:52:45 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 23:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:04:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:07:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:07:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:07:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:07:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:07:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:07:23 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:07:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Dec 2025 23:07:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 23:07:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Dec 2025 23:07:24 GMT
CMD ["php-fpm"]
# Wed, 17 Dec 2025 23:34:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:34:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:34:12 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:34:12 GMT
ENV DRUPAL_VERSION=10.6.0
# Wed, 17 Dec 2025 23:34:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:34:12 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:34:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:34:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fe4e8a27fadeb8a3ecc6ba00a07284cbb35a0c14238e3939a6ad91f917783b`  
		Last Modified: Mon, 08 Dec 2025 22:55:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f511e68f16123650f0819131e26be2bb62a115d515d0e561086c21379d0d859`  
		Last Modified: Mon, 08 Dec 2025 22:56:03 GMT  
		Size: 76.1 MB (76148783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93f5b4cc19a93eb21ef7ed4a9bd397a4b9f79aaff8bb6fb1fa9db9952554c54`  
		Last Modified: Mon, 08 Dec 2025 22:55:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38996f849c1784d7439003696b63059e6bac9d1d9441a0fee62bf01a14f4d6e6`  
		Last Modified: Mon, 08 Dec 2025 23:07:42 GMT  
		Size: 13.8 MB (13760520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ceb88958ddf895481a5efd2aa31cab2ff7247868e77f85511c5697c806c46`  
		Last Modified: Mon, 08 Dec 2025 23:07:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba44490485d03d32d4fbc5133aa6e82c137265058623af48462e52276a9918cc`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 26.9 MB (26910067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725551e40ed3d2e71157388124dd330f4fc45cf0b5a277622d2c2ad2646293de`  
		Last Modified: Mon, 08 Dec 2025 23:07:41 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e268b2b1970fe5f38fe02e171b125e7b6699503e91b174b7bc0104030ca943`  
		Last Modified: Mon, 08 Dec 2025 23:07:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3418808b70657a636ad5df81fcf18597e7a7ca7337f3be4d6bb235ae658e4e`  
		Last Modified: Mon, 08 Dec 2025 23:07:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f281d20bd5608f1e5d13615363f485a785bd5549a7670c38f9e29f74e7253e69`  
		Last Modified: Mon, 08 Dec 2025 23:07:41 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c66565f4e2134f6dcd38af419e393469f2b4f54adb705133937d127e034467`  
		Last Modified: Wed, 17 Dec 2025 23:34:51 GMT  
		Size: 1.3 MB (1271003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baac9bdb8a23e92e74b9d571342260cc78ec5e5137064ce8de001b57ec7ac9fa`  
		Last Modified: Wed, 17 Dec 2025 23:34:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded73026782a34f595c6088c936184c85221f85c1e68892dd69ba96748974e32`  
		Last Modified: Wed, 17 Dec 2025 23:34:51 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc1750f2c9ffdd103a4c2f8df9f8b242748452bde9370719b50ed304b14e48`  
		Last Modified: Wed, 17 Dec 2025 23:34:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf788fe06520c809af0cbf80c88db4ae1953af2921cd9a02e82111c053f610`  
		Last Modified: Wed, 17 Dec 2025 23:34:52 GMT  
		Size: 21.8 MB (21849636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b854914303f79d60d87ab882943b920042f56d4798e5aacf2e51017b75bd9efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57c9aa4db1fa3e4e84726b52ad5586a0549527fc2714d4edd2d59d212016a79`

```dockerfile
```

-	Layers:
	-	`sha256:03057de24edd3871d54e5dd8912fb7319945a1d1bec3f6e3f7648f7c3fc0d01d`  
		Last Modified: Wed, 17 Dec 2025 23:57:02 GMT  
		Size: 6.3 MB (6328760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64759ca1f7ffd5740172db7315caa3c21c505090f25b2ee95a717a6d6e2d4df3`  
		Last Modified: Wed, 17 Dec 2025 23:57:03 GMT  
		Size: 35.2 KB (35248 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:999d678e5e4d411824e0946ddc70c2872662f0ce619ef3729fe1219844708fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193455567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85a705b1ac24ad999b35ad28184a3813808182e5feb53394717a85880ef8015`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:39:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:39:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:39:42 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:51:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:51:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:54:09 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Dec 2025 22:54:09 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:54:09 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Dec 2025 22:54:09 GMT
CMD ["php-fpm"]
# Wed, 17 Dec 2025 23:34:33 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:34:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:34:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:34:33 GMT
ENV DRUPAL_VERSION=10.6.0
# Wed, 17 Dec 2025 23:34:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:34:33 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:34:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:34:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9821050de4b3f0f3739b488b04f69773b014a896bd2c16163dc2d1050dd418`  
		Last Modified: Mon, 08 Dec 2025 22:43:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae77df8ce89f6f900d8846c0cb2de2910e771184b264c30bb5733b50c103295`  
		Last Modified: Mon, 08 Dec 2025 22:43:19 GMT  
		Size: 98.2 MB (98165727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac673eb89e88cde99247263af5433cef453590df5531811f6ef539c8d28e899d`  
		Last Modified: Mon, 08 Dec 2025 22:43:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef745f2c39e3022ddc67cfdcd01a21f2afb91af4d7940d14f789f579de3723ed`  
		Last Modified: Mon, 08 Dec 2025 22:54:30 GMT  
		Size: 13.8 MB (13762457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdbf748657e433630c303a43939438e4c00137752eac850769a81c6df8a0d3`  
		Last Modified: Mon, 08 Dec 2025 22:54:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf371c09d770fea570992f1423414ec052bf19f1e63912345643230ba47948d`  
		Last Modified: Mon, 08 Dec 2025 22:54:34 GMT  
		Size: 29.2 MB (29241160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f5a23eae1729298f94d5e1adc55fae031626142fbf14df915526ac97050a68`  
		Last Modified: Mon, 08 Dec 2025 22:54:29 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1c4b87baf68aef48df6f0964105bee458c4a763226a89dd92492c036b919`  
		Last Modified: Mon, 08 Dec 2025 22:54:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3301d182e890a36f760e0381576efe120d8b64b2352343c1ba1dd09c76afdf53`  
		Last Modified: Mon, 08 Dec 2025 22:54:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9ba9ab6afec1451ef659365c6949f6e13e3c48a38c19ef8c972bbef999ced`  
		Last Modified: Mon, 08 Dec 2025 22:54:28 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b85223398a98ba297344664cc116d56aa3df6e7d990cf1d25a9891d451a5b47`  
		Last Modified: Wed, 17 Dec 2025 23:35:06 GMT  
		Size: 1.5 MB (1539048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460256f8ece53a6c4f107af1f29b926ec5c866a17830f6f6363cea187e6a9479`  
		Last Modified: Wed, 17 Dec 2025 23:35:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9469d52b7055a3357444b71d0173701f46b3d61f27c3f16e09719efd5453dea`  
		Last Modified: Wed, 17 Dec 2025 23:35:06 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48927922bc6fdecc9b6ad1acb3626decc67e2ecc20697d528800f24db90d4ed`  
		Last Modified: Wed, 17 Dec 2025 23:35:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7ab45fdad02746048a71f127e2834191d810e2d8fccb81faf5bc0fd28cbdea`  
		Last Modified: Wed, 17 Dec 2025 23:35:09 GMT  
		Size: 21.9 MB (21853411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f1651707ee9ce077b5ae1acad4db59740e9c43dd74495aed6ac0ca50c1bf8c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6579166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7adcc0b4f1a29d9c3bfe75643a551ec5a66cf86829a14c850842a2dd52c531`

```dockerfile
```

-	Layers:
	-	`sha256:f2627e9879d450b7dab39d836fa2de60c4e5f2056fc74e9e1b9a23bd1ec46b73`  
		Last Modified: Wed, 17 Dec 2025 23:57:09 GMT  
		Size: 6.5 MB (6543877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78bf70872f5b8c16fd0ecc1aabd1d31e2e6eef9fba0807e1a3a16f121428775a`  
		Last Modified: Wed, 17 Dec 2025 23:57:10 GMT  
		Size: 35.3 KB (35289 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:aac723746e41b2638c885431c4f9e268bb605715162d503e7287a51850ba0072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (198959977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007295f2240edd94ac2a71897187e316ab334827c53189d61729401ea46564dd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:44:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:44:08 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:44:08 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 22:48:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:48:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:50:46 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:50:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Dec 2025 22:50:46 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 22:50:46 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Dec 2025 22:50:46 GMT
CMD ["php-fpm"]
# Wed, 17 Dec 2025 23:36:33 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 23:36:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Dec 2025 23:36:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 23:36:33 GMT
ENV DRUPAL_VERSION=10.6.0
# Wed, 17 Dec 2025 23:36:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Dec 2025 23:36:33 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:36:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:36:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c393a4533c93afa5ffe76acc2dbe3bc2ca474b52bd65c5ca160e15e7227843`  
		Last Modified: Mon, 08 Dec 2025 22:47:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74edfe95b6dafd5a8a8790a795d157c7bd375f2093643e2213388318d6bb9a10`  
		Last Modified: Mon, 08 Dec 2025 22:47:29 GMT  
		Size: 101.5 MB (101518303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca091a7ae213f3ae040d65bfa124277519207fbdb1ac811860ab4ad08e10437`  
		Last Modified: Mon, 08 Dec 2025 22:47:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35086995124bc804b8b5735b9c646c8ceb7cb308c799fc33f14e8cf8711079a7`  
		Last Modified: Mon, 08 Dec 2025 22:51:06 GMT  
		Size: 13.8 MB (13761794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b99b22d6c5d888ab31fff4e8151b3ff05153bfc24976677ea8c319076953dc`  
		Last Modified: Mon, 08 Dec 2025 22:51:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5616cd7d8fcff9a70cef666cb865bb5daf9d8b15892509c3ffbc2f5bdebbb0`  
		Last Modified: Mon, 08 Dec 2025 22:51:07 GMT  
		Size: 30.2 MB (30202292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03781d6451ba35ab3b66c7eeff99fe252ecb569bcc4a324ff43476643c5fd50e`  
		Last Modified: Mon, 08 Dec 2025 22:51:04 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c141f929d0c8716bed9c467626a50a6ab7b4b356744d2a57d3ea57878c845d`  
		Last Modified: Mon, 08 Dec 2025 22:51:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a409bba10e84f8ba87cd53d5e55850a4641f57b6e0787044838337cc79feab`  
		Last Modified: Mon, 08 Dec 2025 22:51:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd3b858f06caef14c463f336a746a121fff1d2f1c0d88de3b965ac91741e4f7`  
		Last Modified: Mon, 08 Dec 2025 22:51:04 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b24588283a92e04b639637d5e9173a4f714d9a54367143b3c4b16695f2a172`  
		Last Modified: Wed, 17 Dec 2025 23:37:02 GMT  
		Size: 1.6 MB (1622933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be8408bb9aa5c0efbe3462e1d3cd4f09fdd92c10f645dbac14515e5346c955`  
		Last Modified: Wed, 17 Dec 2025 23:37:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b39eb3b752283c595eceda08ae00526a760f6e88c64c18467154be8c8048ae`  
		Last Modified: Wed, 17 Dec 2025 23:37:02 GMT  
		Size: 778.0 KB (778006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b803b4b1d8b2dc79c9eafa667324d5e13b10d3810aeefcb028b64461a46b8`  
		Last Modified: Wed, 17 Dec 2025 23:37:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2491c55c8b87b84d503936c072bc058d2bae047bb928d1c9e01df70e7b0f778`  
		Last Modified: Wed, 17 Dec 2025 23:37:05 GMT  
		Size: 21.9 MB (21853372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:1725a06237e67584dbd38fe5cf34fe57d0e9e70542d430540f9779210ff166dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6530284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c85025434317f6609156f4610ade9b951aa2f29428eeb4051ffb2b66068625`

```dockerfile
```

-	Layers:
	-	`sha256:15f78cfc804e1c2f73ae8cc70d628dc8d348115ed803e26762228a0c74803d6e`  
		Last Modified: Wed, 17 Dec 2025 23:57:17 GMT  
		Size: 6.5 MB (6495226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6258f52ed12400b68710c29172de25b5bff069389577cc2309b20a9469e688`  
		Last Modified: Wed, 17 Dec 2025 23:57:18 GMT  
		Size: 35.1 KB (35058 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:fc9a428bf3469e0101d1ea2392aa37f11c3fe19cc4817b0330cd7c4a735f3349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204240016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ab8c6d4cec56fb5ff0ddc788e42349998c56c474480d9829e9370b966a7f86`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 12:44:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 12:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 12:45:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 12:45:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 12:45:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_VERSION=8.4.15
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Tue, 09 Dec 2025 12:45:25 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Tue, 09 Dec 2025 13:17:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 13:17:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 13:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 09 Dec 2025 13:26:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 13:26:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 09 Dec 2025 13:26:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 09 Dec 2025 13:26:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Dec 2025 13:26:51 GMT
WORKDIR /var/www/html
# Tue, 09 Dec 2025 13:26:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 09 Dec 2025 13:26:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 13:26:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 09 Dec 2025 13:26:51 GMT
CMD ["php-fpm"]
# Tue, 09 Dec 2025 16:34:34 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 16:34:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Dec 2025 16:34:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 16:34:37 GMT
ENV DRUPAL_VERSION=10.6.0
# Tue, 09 Dec 2025 16:34:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 16:34:37 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:38:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:38:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7fbfa9a935f96015448b226c612416546538a1dcc52e55d20077b60dc138df`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb33d06e000eb34d612247e4138286d5e898db5da65f963214e6d898b0fcd65`  
		Last Modified: Tue, 09 Dec 2025 12:51:17 GMT  
		Size: 103.3 MB (103329018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e40fa0c3ff80077d169fd45b8fbcf082c8de27581241e80d2c54a3edd2591a4`  
		Last Modified: Tue, 09 Dec 2025 12:51:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa9511b6d4007da72abbecad440a5118365615eac2a65b6924c18946001e3f`  
		Last Modified: Tue, 09 Dec 2025 13:22:25 GMT  
		Size: 13.8 MB (13762175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891f862fb58250461b62da38c68d9ad304b72269aa53d0e1dad22900bea6a051`  
		Last Modified: Tue, 09 Dec 2025 13:22:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7420816d357276d8c36b5bddac92911bff1f67cd53d75e9ed1330a633bdefc1b`  
		Last Modified: Tue, 09 Dec 2025 13:27:49 GMT  
		Size: 30.7 MB (30682496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f277ab54f77cfc7ea816e12c9b29fdccf2176a160c4e1dbef245c607ded185`  
		Last Modified: Tue, 09 Dec 2025 13:27:47 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcaff5b75648a36200f5d1a453d81a40436ceb10129a93ceec24c9448351ee8`  
		Last Modified: Tue, 09 Dec 2025 13:27:47 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658e7a9293269f3a9346c599fe9fb17f860da859edcace75249297eda7ac5bb8`  
		Last Modified: Tue, 09 Dec 2025 13:27:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3ab4dd96d296311533e618394b27ccd41258b6d433d072e28b5ec34fba6322`  
		Last Modified: Tue, 09 Dec 2025 13:27:47 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2bce86575a54a436b7970f6a53ac8f1e86bec261fe98e474fb727c88480a63`  
		Last Modified: Tue, 09 Dec 2025 16:35:45 GMT  
		Size: 1.8 MB (1752388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6346d4c68cbc1b5f754cfd0381b714430f1a2dc879c49f1c4c9bcd64bf2fba`  
		Last Modified: Tue, 09 Dec 2025 16:35:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c11285f7c6497cc655dda8373b45ecd2146b7171ec2107f69a2a4fb1e0dd8`  
		Last Modified: Tue, 09 Dec 2025 16:35:45 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f397071aacaa2ffd67993089af1527038fb9aebb90305d75126c05403765335`  
		Last Modified: Tue, 09 Dec 2025 16:35:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcebd7bec57bff6e04bc20e42518238f1715b75dc549c99a4a4e18c413d2e74`  
		Last Modified: Wed, 17 Dec 2025 23:39:33 GMT  
		Size: 21.9 MB (21853536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6c9a00097fbe71fcc2eb2392760548fb8de8415ff6a4ec6065923d3f06bc171d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6525138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe3bb1e03c5a5848db2eb6904570449dca2c939d9d53171121ee152e26ef48`

```dockerfile
```

-	Layers:
	-	`sha256:3afceacb028b878f172dfc5adfb18de4ee4f2f9b23fc4d051dc3dcb413bcd4c9`  
		Last Modified: Wed, 17 Dec 2025 23:57:24 GMT  
		Size: 6.5 MB (6492156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d28c2d29665403e442d10833886bc56d013c15baca4857f2fee634e887b2e4`  
		Last Modified: Wed, 17 Dec 2025 23:57:25 GMT  
		Size: 33.0 KB (32982 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:d5f6abd0d877831f328b9ed5c1a1e33940c6190d6e196522317f0c32ea3fb4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174144587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1016d27990f1821c8011aeb84b0e789dc7602d76cc7695e9e0413d8d11b81c5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:42:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:43:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:43:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:43:00 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_VERSION=8.4.15
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Mon, 08 Dec 2025 22:43:00 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Mon, 08 Dec 2025 23:06:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:06:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:09:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:09:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:09:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:09:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:09:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:09:59 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:09:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 08 Dec 2025 23:09:59 GMT
STOPSIGNAL SIGQUIT
# Mon, 08 Dec 2025 23:09:59 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 08 Dec 2025 23:09:59 GMT
CMD ["php-fpm"]
# Tue, 09 Dec 2025 01:48:40 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 09 Dec 2025 01:48:40 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:48:40 GMT
ENV DRUPAL_VERSION=10.6.0
# Tue, 09 Dec 2025 01:48:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 09 Dec 2025 01:48:40 GMT
WORKDIR /opt/drupal
# Wed, 17 Dec 2025 23:32:03 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Dec 2025 23:32:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31237593c9c01fc9a00d3b7c50c860ac7044ad90bc60e54689865028d0f33ad0`  
		Last Modified: Mon, 08 Dec 2025 22:47:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b459069e89d466ec31d2efb058601341597ff4a8e6a7bcdee371d1f0fc37d`  
		Last Modified: Mon, 08 Dec 2025 22:47:39 GMT  
		Size: 80.8 MB (80826294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbfdd004f8451258a567b001ce3c6509a266cde12878882022092e5d25f9ca8`  
		Last Modified: Mon, 08 Dec 2025 22:47:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcf1555a4fd635094fa42aefd69029f88615fe76173059aa2815eabc7372c4d`  
		Last Modified: Mon, 08 Dec 2025 23:10:25 GMT  
		Size: 13.8 MB (13760991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3cea0a5808e78f0fb6a37504669b731d57ffde7ca308c3a3afee948fac2fcc`  
		Last Modified: Mon, 08 Dec 2025 23:10:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0834dffb978e1ac0168f281d6b1987d2dd5566fe1337cc058071c1e47a98903`  
		Last Modified: Mon, 08 Dec 2025 23:10:31 GMT  
		Size: 28.6 MB (28566290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ab8060add3663a75859a0c490768e6731bfb0a86aa9f1953eb1a0e1dd0326`  
		Last Modified: Mon, 08 Dec 2025 23:10:24 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be86f88c599764ff3d43091a96521000a20869aca1ef0ff513d898e7cfa38ee1`  
		Last Modified: Mon, 08 Dec 2025 23:10:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8549dc912d40983800eb66832a06923d861957986d11cee3f7070e40a1b908a8`  
		Last Modified: Mon, 08 Dec 2025 23:10:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f83b38c901f61651e8a2421134e1580acfd3bec12013ee87fbfe72bd73d81e8`  
		Last Modified: Mon, 08 Dec 2025 23:10:24 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c60bbff4d3db99508462392e92cb2aa28e7e0b96834ce91975b6a0a187f97c`  
		Last Modified: Tue, 09 Dec 2025 01:49:27 GMT  
		Size: 1.5 MB (1461558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd04a7e9c5e94ab980c23f1203d1913ff2b7a2d6b1bcf03794030d143ab22f19`  
		Last Modified: Tue, 09 Dec 2025 01:49:27 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cfec588f00ce9a2ba647f0c0687864e59422759b3da0d6e8159ec5f5d2dbbf`  
		Last Modified: Tue, 09 Dec 2025 01:49:26 GMT  
		Size: 778.0 KB (778004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318ee050f7c437ac78c138fa2505bc21a6b0162e64cf1ab1b65a9bd0f2d93542`  
		Last Modified: Tue, 09 Dec 2025 01:49:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c50d3954e437c940ab2c2ff20942a6a0588c8c5e45831ed62710c2ee564a6b`  
		Last Modified: Wed, 17 Dec 2025 23:32:34 GMT  
		Size: 21.9 MB (21853482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:748516c0430e07c331f36bc9e4a930e4d77c1432505a518ac8354ec23dd61495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bee1f6795efa318da25b8a7af80a888bae3be8037138fcdbcfddb971abc3dd0`

```dockerfile
```

-	Layers:
	-	`sha256:bb8bc85eb43596d834ee8557dfabf70c643b601e94bc5016ea2d989e709dd942`  
		Last Modified: Wed, 17 Dec 2025 23:57:32 GMT  
		Size: 6.4 MB (6352638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c6b36e734acf1460a4089a8536b631466d62632d964d6ff66e96bf306bb3fa`  
		Last Modified: Wed, 17 Dec 2025 23:57:32 GMT  
		Size: 35.1 KB (35105 bytes)  
		MIME: application/vnd.in-toto+json
