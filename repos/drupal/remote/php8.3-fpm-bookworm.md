## `drupal:php8.3-fpm-bookworm`

```console
$ docker pull drupal@sha256:1fabfd10e1ae3333da06c9ab56ebba463187c8159937267caa3ab65acace909d
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

### `drupal:php8.3-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:8c363c29202bceb2c54e2746edb9b7bab996b01d7842791f31ebf1f1e54c7ce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196340779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13576318771f2523d26481d2fcf131b629b234475be1aa444d5901039c5e6d7`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:4d8508b1f217bbb2560830dd12c2a2995d1a0f1916ec66d2e8e7fc842e70ab46`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeeecc41c9a788cd5a18e4ec44256f769c612428a2073c6652a82ab02c1a559`  
		Last Modified: Thu, 03 Jul 2025 23:03:41 GMT  
		Size: 104.3 MB (104331379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec14772bf841e9591c3fd49d61c8ec886fffc5ea2587ea5b1d0c927796f825`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 12.7 MB (12687490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082345387e0e047ffcc42b66b2c813b215835ac08c08e67474a8fcbaa65b2ec`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9668880facffe40d0c21cdfc42a7dfebb945ab68544147f57d77300a4e002`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 27.8 MB (27827689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009fd29da09c1a58c29365476d6bf0b0b74d03898c9f5cc94cf8e1207110ae`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c210824a2f1d29785019f87e2f18b65aabb157c8546094264d4eb6441786bd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f57d5cfefa1dccf4a3cdfba73759d909c5a351bacd670990f1b49c1e2b859d`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958851e84b268638be7f47daedc49341755c74453a9948255a55918ebfd1d288`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb374fe4101369abad7d61f3825b4ad07cc4133e541a6706430a4b4fc19f0f0`  
		Last Modified: Fri, 04 Jul 2025 00:12:44 GMT  
		Size: 2.0 MB (1977273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beefcf6e8becd62640d511b197b542ec5e01787152a5f66e0ab723a6eafb16`  
		Last Modified: Fri, 04 Jul 2025 00:12:44 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d189118a23fbe22d42350b970f07b8742725162c7be98f92f7bdb406d66f2fd2`  
		Last Modified: Fri, 04 Jul 2025 00:12:45 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad5a0b14bdd5fc13178ff57f53628d024f51c8804ad6af6dbca5f37c91f42b`  
		Last Modified: Fri, 04 Jul 2025 00:12:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18f44aa4a31962ca5c226f120cafecd2a821aafde534fbb6f0b97f86a66cc13`  
		Last Modified: Fri, 04 Jul 2025 00:12:46 GMT  
		Size: 20.5 MB (20520505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:c4947a9b024b825fb8564c41eca0d17897c077db1e65d794dc84a5740e87b5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dca06e5cda21d6a6ae169f75c8ef7c3f57c7ee2285e01d598f602e9bbacc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:d83c5ee561550ae09b01fbf59229985385cfcbb85910d85df862f68d5c30c8a1`  
		Last Modified: Fri, 04 Jul 2025 02:03:18 GMT  
		Size: 6.5 MB (6524196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c21dfbae58948d5e32d7468f4fe46bb0fb2364d456cb3bc92ff34085187f3d6`  
		Last Modified: Fri, 04 Jul 2025 02:03:19 GMT  
		Size: 36.0 KB (35995 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:744f8dfa0839a594a432a1c924a2c1a1eee47693dc9ef731507fd15d8dc39eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160800656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcaa6407b2e9997d4aef563eff7f5f488f8a186fca4aab2ad64da5ff08b4658`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:f1f9c8b0a7fe40d2a7e3e984578519d25a9111e7ddde2e00db51f817f0066744`  
		Last Modified: Fri, 04 Jul 2025 00:22:12 GMT  
		Size: 12.7 MB (12685327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1359ff1c99a9917101eb7d6ef46ec5938be21450121902f2685cb30099d1bd3b`  
		Last Modified: Fri, 04 Jul 2025 00:22:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e78de563cdc72f6596af9f2d31e960c20fe392e30399ebe449e12ee467fc60`  
		Last Modified: Fri, 04 Jul 2025 00:31:14 GMT  
		Size: 25.4 MB (25407953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bffd2ca37278db4f72b3466fd5f50203d976105512a455946de42e19a15b1c`  
		Last Modified: Fri, 04 Jul 2025 00:31:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5983b1594801af1294220ecaa8dd33ac4f72a5427163a97fe889e693726fca`  
		Last Modified: Fri, 04 Jul 2025 00:31:12 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2a60e4affe6a73b460aed3d4c1bf4010daa287cfcb55a685db8cf17184e00d`  
		Last Modified: Fri, 04 Jul 2025 00:31:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7edd7a2625aa95786b991d62eb9907c0bb1dde029491a9f32d7110b0d73487e`  
		Last Modified: Fri, 04 Jul 2025 00:31:12 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea63499cda87f22983c3ddeeb419d8d028d825a251ce490f8b33bac46a3bbf8`  
		Last Modified: Fri, 04 Jul 2025 05:32:31 GMT  
		Size: 1.3 MB (1331931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c468a7d4e3399af1bd17bf5c36cbc900042bbce906b60963a990d8e0f5195858`  
		Last Modified: Fri, 04 Jul 2025 05:32:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c35656242140492e63740fb4852ac855efc9b520dc9f36f982cd9a00d55694`  
		Last Modified: Fri, 04 Jul 2025 05:32:33 GMT  
		Size: 752.8 KB (752770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba6af0abc27c3c7f2d43586802972377e21d217a5c3dd2e0e19da259364aaf7`  
		Last Modified: Fri, 04 Jul 2025 05:32:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21c012d021f072b04ccfadc5b973c95b47d1c6a9f7e7de32023bd37730d86ba`  
		Last Modified: Fri, 04 Jul 2025 05:32:42 GMT  
		Size: 20.5 MB (20520770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:d0ef075eef2f591c989c9228bb0fdf61c03bb5705ef90eecec943a95a8bd2e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383767daaec4f21f76c3395bb56577e0dc72e089ea962e4c683ab06f599eaa12`

```dockerfile
```

-	Layers:
	-	`sha256:a213b4aa59146d23d04a3491f2696ba7597ef2791c38da5d89353d6426927eb7`  
		Last Modified: Fri, 04 Jul 2025 08:02:30 GMT  
		Size: 6.3 MB (6337516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80589a0060a6607088aad717d770ef54dec789aeba78c29fe96ce415874f78f8`  
		Last Modified: Fri, 04 Jul 2025 08:02:31 GMT  
		Size: 36.1 KB (36145 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:071899e28fdd798ea998845e817e03d04f0aea25762b7caaf318f0865814a682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190239784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73784b7db6445421ddc98569838f59ede69aba4fdb75018eae80c11673988c8f`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:f37ccd318d109b4a6ca538216ce0795187cc407fa4bd1ff7df4fd2227c107ab4`  
		Last Modified: Thu, 03 Jul 2025 23:50:35 GMT  
		Size: 12.7 MB (12687386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420583571c1c4d29ba15db51d40fa238ffc70b17e6bf1cf93edbe79f7b82c6e9`  
		Last Modified: Thu, 03 Jul 2025 23:50:33 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe605f0e1c8b588bcdc0a8b9f75cda0a5d417403b5b1719bfb92d2d96c8a12d8`  
		Last Modified: Thu, 03 Jul 2025 23:58:57 GMT  
		Size: 27.8 MB (27818292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b693e8b82881d3629f867af10d6d556c3a2624bd28e5ac6ebd6faf7414550ef5`  
		Last Modified: Thu, 03 Jul 2025 23:58:49 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc06dac0b98a962e616d3bc853c53a65a3986cefdd8ec9d65530bcdfab61198`  
		Last Modified: Thu, 03 Jul 2025 23:58:48 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a96f5bd7f6328c52e98a8bd58121b18435aefa72fce2e1b927459c42c54935`  
		Last Modified: Thu, 03 Jul 2025 23:58:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33db9b1576e134b1f8ceeabbb226bf4c849339486ec676a86ce9bb537c8b5c3b`  
		Last Modified: Thu, 03 Jul 2025 23:58:48 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170693eca63425a59e86feb9ef5bf58c7b4819ba3314ecf74b790a3b9cffeb1a`  
		Last Modified: Fri, 04 Jul 2025 08:32:52 GMT  
		Size: 2.2 MB (2239297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615691f4408225cc5ceda469554fe1e09f71cd2b0a05201bb3306a4bf45b97a4`  
		Last Modified: Fri, 04 Jul 2025 08:32:52 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa90b3383739b62f420fda01ec003d88ebf3f3c59ad0a98e2ce57c152e02cd6`  
		Last Modified: Fri, 04 Jul 2025 08:32:53 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497c64499e7b65eff2204405a96a5d5696af73577aa019f20a6cedc89993ab59`  
		Last Modified: Fri, 04 Jul 2025 08:32:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ec2ecb6c080dde5f146b3d1fe2703229d49bc39b6436ea75ffa4e9397c4dd`  
		Last Modified: Fri, 04 Jul 2025 08:32:46 GMT  
		Size: 20.5 MB (20520050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:45123a5edaa3e57213f521a31aaf42c82dc5420da393122bc2ac17b3e2202de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad763aaae4dbf80f3747e01f5ba74b03169fb8107598c4300466f96ccc7743b`

```dockerfile
```

-	Layers:
	-	`sha256:89db232b7b55521dc598bda98bedbfabe32002b089954f5228a64066ddad165f`  
		Last Modified: Fri, 04 Jul 2025 11:02:15 GMT  
		Size: 6.6 MB (6552641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:981458dc054c76766b1d93f349df9a7d0e9b35c22a138477a9c58e47b500fd9d`  
		Last Modified: Fri, 04 Jul 2025 11:02:16 GMT  
		Size: 36.2 KB (36197 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:938430029f31c8e7840ec60a62676739ad51d53310071839f68f8d3435fb20f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195070680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616a89b47bbb87965421a2cc12ca3eaf66e87ddac0d7e4006f88f75e5a0657c2`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:5db0a36f8ca7fcbee6bdbbf455e607d8410275869cf81b39669ba07c3313c31a`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5484c496486beeb54e79a740c20cb9b9c99401862557d517d376f50591b3d0a7`  
		Last Modified: Thu, 03 Jul 2025 23:11:19 GMT  
		Size: 101.5 MB (101515679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c48d4e645f62cabdbd73d543b9ff08bb4b754b481c641cc8fc454ed0ad5c96c`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b97d32edc6ab69ddf9ceba42d5c33b4ddd0cd20d846f7968d6e585c4760d1`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 12.7 MB (12686509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526530c321e6f909004b1cc62ca8761d4cd4e841d8f6d94db6ce7577d0af236`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14315a06fcd54f0c8ac6bb00b78dea1d0532a11306ed5f6919ebfc865593a8c5`  
		Last Modified: Thu, 03 Jul 2025 23:04:12 GMT  
		Size: 28.3 MB (28339893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3f67664f58ea9de571c9b7e853eb3a581b8cebd6f686b0e5ecd0aa3a1e962c`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ae1eea7f16d4a0408fde0ba86dc41eff0b6eb270bd7c440545908312e5d6e`  
		Last Modified: Thu, 03 Jul 2025 23:04:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad31d57fca68deaa8c03f9ae53816e0ce9cdc973a9369ee3451aac413b70200`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc29bcee74fe8b167df4281b2946362fbb56cf138ea86f8da2f4003c2525d80`  
		Last Modified: Thu, 03 Jul 2025 23:04:07 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd017eb6245b79a154d4d7294f2014b5de97b30a0e4ffe68890ad976594eba3`  
		Last Modified: Fri, 04 Jul 2025 00:13:11 GMT  
		Size: 2.0 MB (2029775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10438c4dd4a3959f2f8517b3d30baa36b472476af573a818c30f3e173bf1df16`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb607b4c4ef0503b3086c0796a6a553ac7c52716f56da95d6a1c48d35329833`  
		Last Modified: Fri, 04 Jul 2025 00:13:11 GMT  
		Size: 752.8 KB (752765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3269c1d2e0df88d61eb79eabd0f2623794327d4c82976de9131f2e60cffe255a`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e374bb810e2900b1f1cf991bc1739199d8a0106c93797d8fffed649ae4867b2`  
		Last Modified: Fri, 04 Jul 2025 00:13:13 GMT  
		Size: 20.5 MB (20520094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9d82e9a0bc19ff87e44c777c5b526d62da5966273cf53bdeb9f7554a448e5a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bcb677b58e8474ad2eaecc737e6da9f8ef8b84202db82f4193dfb0b650635`

```dockerfile
```

-	Layers:
	-	`sha256:70f4a4303225d76e16aca87fa280d85e491167cf7dc277f3cd202dc8f884ece8`  
		Last Modified: Fri, 04 Jul 2025 02:03:36 GMT  
		Size: 6.5 MB (6503956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f9e87d491be8ff27b414a0d953cf35daa474c848347a4d229d4eb14af1f2b8`  
		Last Modified: Fri, 04 Jul 2025 02:03:36 GMT  
		Size: 35.9 KB (35932 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:65942fec4b14c07c2c1998157004eb5f67b66947d6468be4f4e69550c144183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200103428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af281b424e8226fbf77c658a9cb820a3fc03d5e7aa1a0bbe47e220b4471f7207`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:66514c684a990ca08e7eec749800a5faf10b8acb6a0c55ca3eb2a0a0231457ec`  
		Last Modified: Thu, 03 Jul 2025 23:39:20 GMT  
		Size: 12.7 MB (12686921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9a02e8c788074b0a26e3dd3863488e62ddcf556c3f445a67ec87c63a5e6a27`  
		Last Modified: Thu, 03 Jul 2025 23:39:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb5c334b2f3259b4901ed42b42203d10a303a7778bab0c3ac4260267e61d50f`  
		Last Modified: Thu, 03 Jul 2025 23:47:28 GMT  
		Size: 28.9 MB (28897064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d356b36ccf840c0bfad0c0eabb5787db4f6c825b30fa6d5e4f85971c11a12e17`  
		Last Modified: Thu, 03 Jul 2025 23:47:25 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc60d360e3324e4e0d3199fbe185117b33e24595349c31a18ac38f3997a344a3`  
		Last Modified: Thu, 03 Jul 2025 23:47:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806109bbc857276283749b65deed217589d677fa58fef033e9c7a672fb1a2a9b`  
		Last Modified: Thu, 03 Jul 2025 23:47:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0066734c9ea6bb94cc861a09116701611e167fd813af872213e9e2ea7afd11f`  
		Last Modified: Thu, 03 Jul 2025 23:47:25 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc7af279d14e3bf63d65f9a2afb6ca42c702cf06b90dbcbeb6a287cec51ca91`  
		Last Modified: Fri, 04 Jul 2025 07:02:01 GMT  
		Size: 1.8 MB (1833376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647e7bbd8f5ed1fbc8f586d30b1c093ee0169e649fe75974a58bcd255558515a`  
		Last Modified: Fri, 04 Jul 2025 07:02:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435fd3746fce4859c8efd148a58e9a20c556cfd9637404d097afad72a6d8bb4`  
		Last Modified: Fri, 04 Jul 2025 07:02:01 GMT  
		Size: 752.8 KB (752771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25e9ec02b5290fb743e86bb787b52f320f56a77014409ff9842cf70df9e2f20`  
		Last Modified: Fri, 04 Jul 2025 07:02:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0db6f480303fe1e698642cf3162bd08bfa713ec4f88433e3c20ff434750f3c2`  
		Last Modified: Fri, 04 Jul 2025 07:02:08 GMT  
		Size: 20.5 MB (20520116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:89d89ee4a71eb5623ec55a69bac3d007ab60eac015f1341ba8c91d083249431e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6537021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5593378f56faee0633a54b02b2c215e9439a6a3010ea957b582d329155d8fbc`

```dockerfile
```

-	Layers:
	-	`sha256:8fc77c74c160af5499862448817bc68020d55294a0732521b3bc4ca9d2981a7f`  
		Last Modified: Fri, 04 Jul 2025 08:02:44 GMT  
		Size: 6.5 MB (6500944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bef965393a52f790e1b59845ca15631159a4bf0cba8f854052d1b9d1ee0ad81`  
		Last Modified: Fri, 04 Jul 2025 08:02:45 GMT  
		Size: 36.1 KB (36077 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:baf96db1dc2ada2ab28cbd2c95c284acdd64a8a9c59796a68e6b511d0bb9eb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170148227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99bb74e5ec3f6fe56f326318e082b829d9acd4756a3f158df7391931f42291d`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_VERSION=8.3.23
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Thu, 26 Jun 2025 15:58:59 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
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
	-	`sha256:0a3ebf93f247acba6ab3f78c99043f126b006b146f2acf92864bd05c0f54e6dd`  
		Last Modified: Thu, 03 Jul 2025 23:42:39 GMT  
		Size: 12.7 MB (12685776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13384d1d46af623c7445a6766c36c97368810a342a0f47fdde6458a4ae17fee`  
		Last Modified: Thu, 03 Jul 2025 23:42:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25491544e8023ea3f987decfb18d8decc127289af7a0051f0cb075e672c27981`  
		Last Modified: Thu, 03 Jul 2025 23:50:03 GMT  
		Size: 26.9 MB (26930621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ef2b2467ba63c7cdd6584406c361f3618047df5653fa9c4a6280f4282a4719`  
		Last Modified: Thu, 03 Jul 2025 23:50:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52b30df120ab60f86b1c7a235173fa75430d23c1832b7f9731735690f5f2d4d`  
		Last Modified: Thu, 03 Jul 2025 23:50:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd0b5c2aa220f4b7b9cab6579235c3287f23ac79db26f2621b5066d4b1b64d`  
		Last Modified: Thu, 03 Jul 2025 23:50:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1b7cbe6854482aa9fabde7670c81ff4ecdc8cb3cd5a05f226791b9cad29f64`  
		Last Modified: Thu, 03 Jul 2025 23:50:01 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ebcae830a66fcb24c55dc824025e631bbcab3ed1fc1333261c05e740c7571`  
		Last Modified: Fri, 04 Jul 2025 04:50:52 GMT  
		Size: 1.5 MB (1531055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378ca56577150066dc43bb68a1f5438ecd1849b653f4688cc2cf62e7737378b`  
		Last Modified: Fri, 04 Jul 2025 04:50:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26d7e88cda059e729de10cb9fa910ac47fd897cd1c624d4ed3bd77bac9ddf4c`  
		Last Modified: Fri, 04 Jul 2025 04:50:52 GMT  
		Size: 752.8 KB (752769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a97aa97fff42aa2884407d00df4d92d9db2e6471481c1537805c8d0c8d7c32`  
		Last Modified: Fri, 04 Jul 2025 04:50:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d032a932eb7c041e0d0b65b6f1e40f26e8eb7158d712257c8c434452d49c13`  
		Last Modified: Fri, 04 Jul 2025 04:50:53 GMT  
		Size: 20.5 MB (20520857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:daea0c115af2f9a1685265d8423c28a13e71071fa3c34553666cd5a6809cb65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d63dc669d0fa131aeef07ce3d912a62783b0b292ecca5a8aa4d7dcb418946`

```dockerfile
```

-	Layers:
	-	`sha256:3f089e29ea2d16ee9bb973c6a376754a3c9d53db30abe9a51e8fff546d6466e2`  
		Last Modified: Fri, 04 Jul 2025 08:02:50 GMT  
		Size: 6.4 MB (6361414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51f803ba8a1609abc7e69086b68851f956c7193ac5c3d43660eb6810bd5fb90`  
		Last Modified: Fri, 04 Jul 2025 08:02:51 GMT  
		Size: 36.0 KB (35989 bytes)  
		MIME: application/vnd.in-toto+json
