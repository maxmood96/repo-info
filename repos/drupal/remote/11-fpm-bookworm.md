## `drupal:11-fpm-bookworm`

```console
$ docker pull drupal@sha256:8ac7933487cb2b07b658dbffb00e6274d3f835bfb3d988dd419bfe3a6aff7b3c
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

### `drupal:11-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:cbef9709470ab1adbaaf460d0daf717ab2b3f292b724d2415c41c961e1a2854f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198884906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8082bffefa3b44ecee64a64edfd21b19e7e576c09af8e4465fac1271db6f61d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:20:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:20:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:20:26 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:23:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:23:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:23:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:23:14 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:23:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 00:23:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:23:14 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 00:23:14 GMT
CMD ["php-fpm"]
# Fri, 07 Nov 2025 00:40:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:19 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:19 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ebf7026885071d49c485c8938caa2cff6be77e5b94c84be9a53795ce6c76bc`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd66f4ec9faa17fbe4c84c32aefdf9b2e0d653efab2437c3ef4c38e8e42db5af`  
		Last Modified: Tue, 04 Nov 2025 00:23:55 GMT  
		Size: 104.3 MB (104330563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4b314c6fa53293a89bd366e7cfa8d3bab20b4dc43288578412b2f4bca4058f`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274694c2b656b64ed5b8931d4798b960ead8c23560bb4b0917a6be687598d830`  
		Last Modified: Tue, 04 Nov 2025 00:23:46 GMT  
		Size: 13.8 MB (13754324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d806af479a8519c955ea1dbc61063bc511402200d0f5b3123052e7bea876fd`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fe26a54d31d52f56c2be6df98731f7806ac934fda7cc5368b788799f6b6092`  
		Last Modified: Tue, 04 Nov 2025 00:23:45 GMT  
		Size: 29.6 MB (29612115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afbf180cc08ed00c5c4ec52c75a7fd63ba67d04991ccab025b5d16351b4fdd0`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340bf8f26db5cd0368981809e2b9d3555ace369b50deb06da739a199bfc58a09`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f362207e68bf8301b94c90e325d4928ca296334317afc4a66aa9119a5bc7f137`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046fb614a7486f3af1fc90a1da8a3700a70fce5f8e67ca2b5ca65d9be250624e`  
		Last Modified: Tue, 04 Nov 2025 00:23:43 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10011c0ba02ffce63e27e36b1afa0e53f142fc41c976306316fb68c3a61516b9`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 1.6 MB (1550570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d696b4750444cc1cdd3a0d6224513ad321f6f5f92595903261826d8a60dcb7`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806706208072aee908e691731a98734c5c95b8722616628180bc69d33d9376d3`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 751.5 KB (751482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945cf88a3205a4491d4aebf356a0774fda7d80ac99735d0236a3e47374a11aed`  
		Last Modified: Fri, 07 Nov 2025 00:40:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3d13b2568a13f20b4b810c52e52425fb32e88c6a7817d1875b4bd0d01a8555`  
		Last Modified: Fri, 07 Nov 2025 00:40:51 GMT  
		Size: 20.6 MB (20643753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bcbee0e98a98e227372cb4dfdf9eeedcfe19b68bcb70b480eddc9ce12d1d6ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6562228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00383ee436ebdd3e254510371c408491fe83f97e8cfc5d952325637143df656c`

```dockerfile
```

-	Layers:
	-	`sha256:b91285634a45a857ff2a8dc422a7db6fbdfc10ea5f0a2cb0c906f6b2d8ae7317`  
		Last Modified: Fri, 07 Nov 2025 02:58:56 GMT  
		Size: 6.5 MB (6526329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b93d4ef107e204687017b1adedb52c4e5e238bf93b8eb766ac9f892769f05e`  
		Last Modified: Fri, 07 Nov 2025 02:58:57 GMT  
		Size: 35.9 KB (35899 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:372e26d8725f9774775aab734b63c7f854f668bbb95e2ba4b6e5bff29ebae9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163424388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038f769c6e11f532fae63dc18ba3dc2df27304c52cafa022e01b93b7e1657acb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:16:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:16:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:16:29 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:20:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:22:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:22:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:22:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:22:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:22:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:22:45 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:22:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 00:22:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:22:45 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 00:22:45 GMT
CMD ["php-fpm"]
# Fri, 07 Nov 2025 00:40:21 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:21 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:21 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:21 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54af4eb5e0e04389bb5e09cb092b01585155c66cd4058a46a72ab4d2951f7c`  
		Last Modified: Tue, 04 Nov 2025 00:20:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ddd5e6df0b4516c049d2bc8079814629f310023faf49e45bbcc3128dfa5191`  
		Last Modified: Tue, 04 Nov 2025 00:20:09 GMT  
		Size: 76.1 MB (76148678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3035766ac35e75ea03d833ce9b9229c93fee7661575c621f16067bd3de8c9da7`  
		Last Modified: Tue, 04 Nov 2025 00:20:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364977cb7dafbba537186978923d84ee26eabbf96d915983ea2512132d0c603c`  
		Last Modified: Tue, 04 Nov 2025 00:23:04 GMT  
		Size: 13.8 MB (13752199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71eeb492b71502831ee67e22772b8645d7ad18fc1d15f8f097ee2c82b495c2`  
		Last Modified: Tue, 04 Nov 2025 00:23:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ef921f1b2b12539bc3e37fe774d4cb2e8ea32db89a1e89844eeaf49bbf4544`  
		Last Modified: Tue, 04 Nov 2025 00:23:06 GMT  
		Size: 26.9 MB (26909320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb88356457799ecbb077a557e87a043b88dfb308b98f9dc80b386d3a851b719c`  
		Last Modified: Tue, 04 Nov 2025 00:23:02 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a1518446c3131968e08069306db1fe04f823b76ff1b2f1b7774959800bcdcd`  
		Last Modified: Tue, 04 Nov 2025 00:23:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9b3c934bcfe2d44e69e3ce7908780570715f0dadd282538c1d5aa8c27a0c93`  
		Last Modified: Tue, 04 Nov 2025 00:23:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e7e84cc7a804b60cd898f7d5a142252e6cfba7081dc5e4816521482260f5c9`  
		Last Modified: Tue, 04 Nov 2025 00:23:02 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356d8ade962b1b37b9867cf74368814e6daa6603a3eba5ee23a3f93f713da8f8`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 1.3 MB (1271282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e158bb50d55f0e4e783373050373e57b4df26929e69350fb4c133e104f62858a`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868dd11685ada30c012f961ceb0f0ae8a462b5fd1f15439894f93003393d5a9`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ef9e7437f1dcfc1559aa3613d7c466d4db9b99cd2cabea9b678fa4faa07cf`  
		Last Modified: Fri, 07 Nov 2025 00:40:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3cbd3bfcf3143980018db6ee746c6a54d7b058d8df923140256442ed6cdfa5`  
		Last Modified: Fri, 07 Nov 2025 00:40:59 GMT  
		Size: 20.6 MB (20643767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:df23b872e8bb8d49c536a140dc92b3a38c1e020bf8e6c6b73a6a12008b9a6b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6375703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44d83e1846032e1e05b2c8df77e78e71e22ad34b8e1e521a0678d1d288909ca`

```dockerfile
```

-	Layers:
	-	`sha256:e65c3f5ee87fe24d1bcdfba66c133d5b35e865168c0192b1729ddeb95073167e`  
		Last Modified: Fri, 07 Nov 2025 02:59:03 GMT  
		Size: 6.3 MB (6339649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d13e0f64615183399f7fbe6f7e8749559487134d454ed4d9a76297e77f79cb`  
		Last Modified: Fri, 07 Nov 2025 02:59:03 GMT  
		Size: 36.1 KB (36054 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c288d22a9f9918b04e4fe595325358dfbfa40113a267f0f18147355ed920aec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192205327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487081dd0054c50abc08d5480f971a47ea4b2af54a4380053e61185c601a52fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:20:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:20:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:20:38 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:20:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:23:38 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:23:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 00:23:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:23:38 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 00:23:38 GMT
CMD ["php-fpm"]
# Fri, 07 Nov 2025 00:40:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:29 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:29 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:35 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8b335248716c4b9365851d8592510a6cd88af276235a771a0ebb9f4f424282`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def314a06948b06daaa4c8111bba98c42985f6b0981ed71c13c19eb208b1c21c`  
		Last Modified: Tue, 04 Nov 2025 00:24:15 GMT  
		Size: 98.2 MB (98165674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b81acd8d5011518e5e93f41d5d8125f09e22c4c9670e3fb8097c4c8706bb6b`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36af371db4defc86af8b5b7033433925400cfbf48fb63a8fbd75c90856622ebf`  
		Last Modified: Tue, 04 Nov 2025 00:24:06 GMT  
		Size: 13.8 MB (13754133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588165812f31aee011905152ecc47e370a5bd52089bc18a6b8de66da35c48b65`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2fe6c7972ba3389d4d7734288ec45f4c3f096b803527e95ac879afed32694`  
		Last Modified: Tue, 04 Nov 2025 00:24:09 GMT  
		Size: 29.2 MB (29240613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9f1e175405ffb016a080c059c7ea27ee551ee0c50ad4e0f0353c45b5d66eb`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f6b51456504de5e79a3972b285f799aa8c63472d4b752a9a2566382eb5c1b`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b54cc4f4fb6961347b80701a83ef7e3b2fadc013e6250fa5218a381b8125cb`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ae270b1eb124e202b2824a2578c7186359bf45410c168dccd9504f59d36455`  
		Last Modified: Tue, 04 Nov 2025 00:24:05 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a88672a8bf1588d0ae1c0e5545c21fdc67f4a16c959b9905de823fe41f49ba`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 1.5 MB (1536175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b220ff946d80ee775fbe27322af294603203e35b826c071b52a270ba92f4f55d`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f05281bd9476a87547e04d39c5b55f414a1a19bcfa3cc5a56e27fb05e2ada4`  
		Last Modified: Fri, 07 Nov 2025 00:41:01 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08e0a635a4914e8628812ca9cfa992e35e07a8d08c9133818c335e8f5c86e7`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32b73c2873cbb0c628f0ea81595017f30e21f1030b9401388e6857f24c95b8d`  
		Last Modified: Fri, 07 Nov 2025 00:41:03 GMT  
		Size: 20.6 MB (20641333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b2d5682a179d8e0ab91d3344e44d79383fb2e5b59e2c4cb59c783590c5cea347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00debd683a77e589ff253b5c70d3d97a64ed2ebcd8639bd58318505fb87dffd9`

```dockerfile
```

-	Layers:
	-	`sha256:b80b8eb36b097541d39707c79172518a78ac9d253302ce20280c9c3c103c23c2`  
		Last Modified: Fri, 07 Nov 2025 02:59:10 GMT  
		Size: 6.6 MB (6554774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b6f6c184b7077b41e8c365ee02b217e14c9f254df5178f621b93e575d529e2`  
		Last Modified: Fri, 07 Nov 2025 02:59:10 GMT  
		Size: 36.1 KB (36102 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:5234002db241ba7c61d8d6b84b9151025dcdf43694c84a33d07cc2c3e6e1b8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197714839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85ddfcd7802217b382714a57eda72e2c43a166bc9cb440c38f244df02b9f5e6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:17:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:17:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:17:37 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:17:37 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:17:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:17:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:20:13 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:20:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 00:20:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:20:13 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 00:20:13 GMT
CMD ["php-fpm"]
# Fri, 07 Nov 2025 00:40:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:38 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:38 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:41:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:41:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0230a32fda43d4ce86df15ef793926e3e2ba734cb6cc7c2cad75e27e1fa2bd6`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c944c6ca2c2c7359770a013834e8fa91b686706432618ce0f6c68257cd56b935`  
		Last Modified: Tue, 04 Nov 2025 00:20:54 GMT  
		Size: 101.5 MB (101518592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08074997788c035d5dc3383d0d5db73203b83eb8594fb28b07fb3ade6d4a5fb`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cd1241da56d0a4bcfaf214c05c70e4ce815f913d25bb456c6f8f7edc49b6e6`  
		Last Modified: Tue, 04 Nov 2025 00:20:43 GMT  
		Size: 13.8 MB (13753507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecd266f3e5d8502e7278afbeeb725ebf27bb45b794a663af3308d30ab1b7c6e`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f526ad82463bb053796bd91c6f30f6b122f8cd1c8c90a23ba77468d71502015`  
		Last Modified: Tue, 04 Nov 2025 00:20:45 GMT  
		Size: 30.2 MB (30202686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda642b2f450751761d3fedb92872226980e8c7e6f73c91ca4fd4e990f45cf2`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ccd78ca288f304175944aa6826a8c008375ab53d77e60c297e2a20a411f0b`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefd67bab6bfbc5145a9e5ab834d0f3ccf24165b42c1f39cc9fc2c4022960f31`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeda7c4e13df279737417ef4490502be83767b3aab74936167a2c07531801b8`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9b59a651f677f5bd1dd21dfb47dfabdee0d542069b349c60e40785d28b3d83`  
		Last Modified: Fri, 07 Nov 2025 00:41:29 GMT  
		Size: 1.6 MB (1621988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c505f7a1fb647b2b2c6119d1f1fcf5b0f4c2d41ebe26081cc2a79652cbefad56`  
		Last Modified: Fri, 07 Nov 2025 00:41:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75f3955d2aeaca2d57b3103bbfbb175e47fde630c21aee383609d4b1b21562`  
		Last Modified: Fri, 07 Nov 2025 00:41:29 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d1fd8ea22ac0022f0053d16360f81295784b16a11a170d7c71c2682d58b001`  
		Last Modified: Fri, 07 Nov 2025 00:41:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3489ffc0c2a2774d22daf341ecde13a89e963f52222a5bb96200e28db0d4002`  
		Last Modified: Fri, 07 Nov 2025 00:41:31 GMT  
		Size: 20.6 MB (20643206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2c8f89f57d19d3e09e8a814cc3f217c2be7c0b3f3e216057e3b29da57d433ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6c13d4aceec7fd3cc9730083a5684c436d5aac44ded4212d2141101fd608d3`

```dockerfile
```

-	Layers:
	-	`sha256:16b6861461e03a3eaf31d942510f56664d1c83b904d5ec749f2cb13c1e5db4f9`  
		Last Modified: Fri, 07 Nov 2025 02:59:16 GMT  
		Size: 6.5 MB (6506089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6a45c3faae030f34c54f5fa2706d161b428a193fc66b3027be08b93212fd23`  
		Last Modified: Fri, 07 Nov 2025 02:59:18 GMT  
		Size: 35.8 KB (35837 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:87a349436a3f861ba4d51e101e3275f5ef3c589826cfafb36f4f5b6b8d503986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202993543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9094cd3b3c6c2cd71df9d03590cfcaee58fb32f4e621677e4c50564f34b292e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 02:33:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:34:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:34:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 02:34:19 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 03:30:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 03:30:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:33:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 03:33:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:33:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 03:33:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 03:33:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 03:33:58 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 03:33:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 03:33:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 03:33:58 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 03:33:58 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 16:09:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 16:09:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 16:09:42 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 16:09:43 GMT
ENV DRUPAL_VERSION=11.2.7
# Tue, 04 Nov 2025 16:09:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 04 Nov 2025 16:09:43 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:54:21 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:54:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423ff8a5d9e5803ce51c4bee23a305ce775f33ac0e1498c84052d0e8fbeb72c`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d4bf9d38282d902e4e65ff38ac946e13144e841061113ca97aee44f4413c20`  
		Last Modified: Tue, 04 Nov 2025 02:40:57 GMT  
		Size: 103.3 MB (103328858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b331438757ee31483215b6dd106186ef28c3d99b0849f835e85e4cba07a27b`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4078e91c0f552dc18dad8f93d7e0b7000b7c191d61c14a6c681a5c2e6083b`  
		Last Modified: Tue, 04 Nov 2025 03:34:38 GMT  
		Size: 13.8 MB (13753770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d305004bccc5ca5e14adae67bac7d9ff42988450f9cf771189871d51e3bdb11`  
		Last Modified: Tue, 04 Nov 2025 03:34:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e0e03e497933adaddfa13840b6881045453c1662b721bb6092c6a79ceebe1`  
		Last Modified: Tue, 04 Nov 2025 03:34:39 GMT  
		Size: 30.7 MB (30681448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51e53ca47c44358359c1bcf2faea512bec1d676066df8dc9f6a4f533220e179`  
		Last Modified: Tue, 04 Nov 2025 03:34:37 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6ab50c8459435c40efca3a11ecba9fc6b819f3869efc64a0a76c8b1e7b041`  
		Last Modified: Tue, 04 Nov 2025 03:34:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bce9fbb3203d100914a53332d264d8d045e1e030fa6377596ea191151feee9`  
		Last Modified: Tue, 04 Nov 2025 03:34:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87bf4041b07be852455efb76d306572c983dafd37da204e9265babfeff853f2`  
		Last Modified: Tue, 04 Nov 2025 03:34:37 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97c1a3b1d1dd8c35e8defb1b823450bfda1187013599f9589f6480295325b42`  
		Last Modified: Tue, 04 Nov 2025 16:10:52 GMT  
		Size: 1.8 MB (1752004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7db449bdb962870cda3383bcc69350221ab9c74ae1b67cd8c6d7e2ac34db5`  
		Last Modified: Tue, 04 Nov 2025 16:10:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6fd2874141bf006fa0907d9bb8a70deee1dc387ad1dcab2619a49bbcaa4655`  
		Last Modified: Tue, 04 Nov 2025 16:10:52 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d45d984e3df05461d0aa3a121c97a653aad3ad64c29a9b8bcbecfa18358888`  
		Last Modified: Tue, 04 Nov 2025 16:10:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6519a9fb1757c3d9e9dd5038a8fdc54c97947e1afcb4466f96b647f93b0ba6cf`  
		Last Modified: Fri, 07 Nov 2025 00:55:12 GMT  
		Size: 20.6 MB (20643540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:492819723d67c21ebbc6f8a735f702003e8cc1d399ee2350c20935d73e968f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664773c08eced79704ae266dd872f92755c5e47365feaf4fea50a268cd82e493`

```dockerfile
```

-	Layers:
	-	`sha256:ed3b9dd9867f5195b21faea5eb55ff9b1b350b4629b7080e763d313b53eb08a5`  
		Last Modified: Fri, 07 Nov 2025 02:59:24 GMT  
		Size: 6.5 MB (6503077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f87ab46b3520087504c9e901b289b6d4cde58a35ce5e7e2fb8c6240fc6da2f`  
		Last Modified: Fri, 07 Nov 2025 02:59:25 GMT  
		Size: 36.0 KB (35982 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:b2845b07b87cd1281069b845b83a23a0d5b1c359ea40718d9299c74e85fc6883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172899409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36545ff6600a9d13346e05b876efdd9b6a093721a1d098fc79696be5f119bf60`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:30:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:55:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:06:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:06:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:06:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:06:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:06:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:06:07 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:06:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 01:06:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 01:06:07 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 01:06:07 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 10:06:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 10:06:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 10:06:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Nov 2025 19:29:11 GMT
ENV DRUPAL_VERSION=11.2.7
# Thu, 06 Nov 2025 19:29:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Nov 2025 19:29:11 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:53:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de54dbb81980c9b8d3c221063f25b8474ca2be777ee639ae7b090f0b6933433`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3263ba1b0b7542bbb392f8a89ebf9d5562c8e7a8d05dd575aaae0c51490011e0`  
		Last Modified: Tue, 04 Nov 2025 00:35:33 GMT  
		Size: 80.8 MB (80826218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66245e37d456fef550ca4136b0b6f8bf79ff609208f0f6a1a952faf0bd6a42`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9a490a5132003231ec42078e93e42e97bd14203e2ef5104aa8626ee4b7ba1`  
		Last Modified: Tue, 04 Nov 2025 00:58:59 GMT  
		Size: 13.8 MB (13752711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b39e9fabec86a99490b3e8bf8d063897984efa9b58bfb7545b56b52de703cc0`  
		Last Modified: Tue, 04 Nov 2025 00:58:58 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4847a825d17a30041d87248e3286269874fe7c22aaf7364f77d20c6a682d48`  
		Last Modified: Tue, 04 Nov 2025 01:06:36 GMT  
		Size: 28.6 MB (28565930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc7b9fb147bed4509f2ca106b8541c1dbc1b49a7248be7440190e23992e6cd5`  
		Last Modified: Tue, 04 Nov 2025 01:06:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebb88747135f01f6a32f71c9e470f4784a91c6616f043863b9aaf206a6740e8`  
		Last Modified: Tue, 04 Nov 2025 01:06:32 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bdba413a43dffd7695500b6fefbd948f73596ecd54500fcdf90c7d4eb0bc94`  
		Last Modified: Tue, 04 Nov 2025 01:06:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237515a330747637d80567df434340a89b59a033ab08733d9c0140c2e5be4a59`  
		Last Modified: Tue, 04 Nov 2025 01:06:32 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8628197a1f96be6ed5e2d0e19c02f3c18a4f004ff1588f8965ffd65e1876bbf`  
		Last Modified: Tue, 04 Nov 2025 10:07:11 GMT  
		Size: 1.5 MB (1461447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d053e2cc6df11f1fa228da40f70dbaa92794c08ac22e8104d6b47536ce6a20`  
		Last Modified: Tue, 04 Nov 2025 10:07:10 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99918b5916fe759d9d6f88abb266dc30347b281c5452e80b7e2326c51edba8f`  
		Last Modified: Tue, 04 Nov 2025 10:07:11 GMT  
		Size: 751.5 KB (751480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eb3682df2258b4bf88e0bd9644d801c3e9ea8bad2d89c52cb3c08530886861`  
		Last Modified: Thu, 06 Nov 2025 19:29:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21170367f4575aa2f223bb78a42c2389ddb0a58fed50bedab2afa51405f7715b`  
		Last Modified: Fri, 07 Nov 2025 00:53:36 GMT  
		Size: 20.6 MB (20643532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:410b5e304699a927d6ce79852889b888dcaa51a8b8474c66dd0bd77287895210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6399441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b29fcfa979f1ebe738d22fb549e852a51ebcf592895326bcde7f13b229725`

```dockerfile
```

-	Layers:
	-	`sha256:54792ce781aa7babe6c39b30b0fc74771386dbcbbfa61b6de1a793474378f9ca`  
		Last Modified: Fri, 07 Nov 2025 02:59:30 GMT  
		Size: 6.4 MB (6363547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eabf979fe0613849e8e3c7900686773b588c7c737f9ece7f8d660771359fef4`  
		Last Modified: Fri, 07 Nov 2025 02:59:31 GMT  
		Size: 35.9 KB (35894 bytes)  
		MIME: application/vnd.in-toto+json
