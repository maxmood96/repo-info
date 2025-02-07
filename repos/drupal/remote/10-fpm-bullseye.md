## `drupal:10-fpm-bullseye`

```console
$ docker pull drupal@sha256:81a3bb2b0257b9b38d25cb4df4f8ba7f3875bfca6ae6527506c7dca6f1a94725
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

### `drupal:10-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:b349a81d7cd66b67834cc1b017c4dd0b8e5e5d8222ab5533340d840939882096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185046064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c7e15c5752123a3fbab85f4cf478a848ad3b871d0d59af49f497e900b903c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b15f296d1ec744c2be172e144abe941671d8b29fbf977719ceff9277e3510c`  
		Last Modified: Tue, 04 Feb 2025 04:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9f3dcd6d3771671e1caebcbb522d1d8df45e57b76721695ec8bbe9426f4230`  
		Last Modified: Tue, 04 Feb 2025 04:37:08 GMT  
		Size: 91.4 MB (91448426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d47eca7dd0e3b12ff62dbc1910f7ae16a4294b9a149a21d41586f631438e1`  
		Last Modified: Tue, 04 Feb 2025 04:37:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ba3feed7fd714ba01d58fdd9f595640f130dd99a659066e20e8a1ee30802c6`  
		Last Modified: Tue, 04 Feb 2025 04:37:06 GMT  
		Size: 12.6 MB (12647832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f2de16c3214b4ba09e609311b1b7675ca7448a5a0d1c348c41e5ce20c0e9f6`  
		Last Modified: Tue, 04 Feb 2025 04:37:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e830a01c0b8c3e8ba5f501a9b25f523993038f9deb6e8ae44919b2676e4c98ae`  
		Last Modified: Tue, 04 Feb 2025 04:37:07 GMT  
		Size: 26.6 MB (26556905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49acfe614b1e39f9fc7fcb58b044e4909e47ddb854b819cf0d2c63b3c7cf797`  
		Last Modified: Tue, 04 Feb 2025 04:37:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453adfa95ee64b507a414b357e52f29e756e8a2f792e6fd7b040ab6d0155026e`  
		Last Modified: Tue, 04 Feb 2025 04:37:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a9d88f6898d03392295593946008dd5b25e8212dc818d87d2239f40233c2`  
		Last Modified: Tue, 04 Feb 2025 04:37:08 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db4199e6f030daa6e4b92fa394e6cd8aabb1b24cd4d303c88138e8a9f66e67`  
		Last Modified: Fri, 07 Feb 2025 00:28:58 GMT  
		Size: 1.9 MB (1906940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9aaa98c2115cd5adb45b13ad73136d70ca00a66d389b6d8ab8884ba1bf53fe9`  
		Last Modified: Fri, 07 Feb 2025 00:28:58 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af12c4f9dd5b5b0a223fa30761ae7e17ced3df4684de79916e511d2143425c29`  
		Last Modified: Fri, 07 Feb 2025 00:28:58 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d1c96a46cc5035ffa74c2fec576c6598a859044f20fac0984ef91bb5c2487a`  
		Last Modified: Fri, 07 Feb 2025 00:28:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb662fca6f04427e8f0b8c7086f26a589f0f548de3bba990fabb8f304ffb9a4`  
		Last Modified: Fri, 07 Feb 2025 00:29:00 GMT  
		Size: 21.5 MB (21479759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a05a01f901c269ae3117efdb977ec065b69a56b24887a1963f700238821250af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a2cfc5b694a2a70073a6d1346e302937970bf603a59d0c6a2bec488bd7c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:637a47d5aaf1e2251234dc1deafe7f3046214dcbcb260930269578b1b89a9f38`  
		Last Modified: Fri, 07 Feb 2025 00:28:59 GMT  
		Size: 6.5 MB (6482872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd2e897535bc88e82fa71a64e2fa561e7137d9ba4e8849f0be6d1d0d8181211`  
		Last Modified: Fri, 07 Feb 2025 00:28:58 GMT  
		Size: 34.3 KB (34291 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b1535b57c30aef1ce2701334aa2fb4a77e8a3c01b0ce4727e49e4418e0283bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155060160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a579858bd0b93df317524f663866f9ce0e35d55da7434c6f45ab17568c53691`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
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
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9f22afe418a45c031cf43983b6e05c8ed9b386411bd488f375251dc4089c49`  
		Last Modified: Tue, 04 Feb 2025 05:25:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20b645f918db98d26680f3077f4791bf599ff64dcf689b13a40c8243399e230`  
		Last Modified: Tue, 04 Feb 2025 05:25:06 GMT  
		Size: 69.1 MB (69119296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03588c4764681ba1b285def08d8bf43afd148e8bc56a103b85f5ac8fd68cd75`  
		Last Modified: Tue, 04 Feb 2025 05:25:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bce3f452c99552ff8ace4c571c2d3223398bc3cf5621f1fe448bbadf41fd45`  
		Last Modified: Tue, 04 Feb 2025 06:49:19 GMT  
		Size: 12.6 MB (12646374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79287f5dca111d34fe877673d0eca4adb8393c751abfc3731ad3dcd29817871a`  
		Last Modified: Tue, 04 Feb 2025 06:49:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54140838844153c980bbdb115352e3b207fc60aa4df9eefc254b6fe18cd48c8`  
		Last Modified: Tue, 04 Feb 2025 06:55:29 GMT  
		Size: 24.2 MB (24241332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaac20a3e7988da04c1ec366e0677ad8f43d178c7a4eade4290305fad854fc2`  
		Last Modified: Tue, 04 Feb 2025 06:55:28 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3d18475c17f02098739d605300de9c8dd77e5da6c377be83fe449cdbea6ce1`  
		Last Modified: Tue, 04 Feb 2025 06:55:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dbc3e3c9e4cc0da8f262cf7132d9d541a6a3d7d14563dfe12b312102b32f81`  
		Last Modified: Tue, 04 Feb 2025 06:55:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edad75a4452c1162a29ea7e1a2e94c55b89f08f6dec8b84369b7fc2a85d95226`  
		Last Modified: Tue, 04 Feb 2025 16:32:32 GMT  
		Size: 1.3 MB (1285805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81ca274c39fea013f02e77c03a7ce9121529504f8afe8b3ae4ffac86381025`  
		Last Modified: Tue, 04 Feb 2025 16:32:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f32534a51b1e2c9195acbf424d39a9ff90b10e1460c3eddb6ffa7cc1ed153`  
		Last Modified: Tue, 04 Feb 2025 16:32:32 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784695039a08edcc2ab6e935636033cd8d172ffd1e46b2ee10376e4ab40655d`  
		Last Modified: Tue, 04 Feb 2025 16:32:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07a16e8bc6c3b531bbeb7a1996e5d97b19922dbfe551d344935266a8ed019a9`  
		Last Modified: Fri, 07 Feb 2025 03:32:28 GMT  
		Size: 21.5 MB (21479850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e1917d5181776bab926a2730625c8f6e8b413046c8a7840c1b2e0393ac6fa345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811923a1c3eddb88cda57111ee21272f00063b4b060277ecaf2740b64f069967`

```dockerfile
```

-	Layers:
	-	`sha256:761d5911479ee0f4202dd9ee39351e6c673184cedd44b13351455c2f50bff57c`  
		Last Modified: Fri, 07 Feb 2025 03:32:27 GMT  
		Size: 6.3 MB (6301821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4055412a8179553633361eecd24ef3e9aae8a77f9f28c54a971eb777f97b3e0`  
		Last Modified: Fri, 07 Feb 2025 03:32:27 GMT  
		Size: 34.4 KB (34431 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:dc8ba91ceac33a912402c83bc7c8c2d0c6516440ad0dbfa97068b699568b2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179121907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed90a74c1438f6e9a54d863874c4d19d48faa67a5e5f120898f1489875e78601`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be641d1a0556ee0ecbd75f2b0e73635549d09ef2fe2be21d868ca13a1c6db1a9`  
		Last Modified: Tue, 04 Feb 2025 05:31:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1983ee03492e8aeeeb44d7c7385775b851e54d50f21c9617974ec1d2781d7dbd`  
		Last Modified: Tue, 04 Feb 2025 05:31:55 GMT  
		Size: 86.7 MB (86734294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def08e85306c2376328c5349bb03f55fb95a407d80e3c68b4627678b99683827`  
		Last Modified: Tue, 04 Feb 2025 05:31:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0591fbe4aa9ac96f1bd479bd14735a098f6b9626b3ee2daa7d18217693fbc6a`  
		Last Modified: Tue, 04 Feb 2025 06:59:43 GMT  
		Size: 12.6 MB (12647255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9230d684d84dae69cc2b204ac10cd347708b7d7bb1ba62319ae84742e44ef646`  
		Last Modified: Tue, 04 Feb 2025 06:59:42 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafdc1f2f96bc70747edc041c56f99c158f7946f3c342070946cf31d63228cde`  
		Last Modified: Tue, 04 Feb 2025 07:06:58 GMT  
		Size: 26.6 MB (26591641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b495db7fe2320fc07df2dc3032b4cbbb85926fba7ac410438f9bb5144f4873df`  
		Last Modified: Tue, 04 Feb 2025 07:06:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb06aaba45d01b22ea6d10413b3ed3416d8a31efcebd9865a0b7054f97d9b80`  
		Last Modified: Tue, 04 Feb 2025 07:06:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb21e71a76f4b43c77b781c6d8735a3db9cae97d29606516eea1a8f145e750`  
		Last Modified: Tue, 04 Feb 2025 07:06:57 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162fa3379dca48b27f2fd40f1bef1058afdfe0329bc1e0332429cf89781f80e`  
		Last Modified: Fri, 07 Feb 2025 01:55:03 GMT  
		Size: 2.2 MB (2170782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bfb93876e4dd4f2bdab62781d5aad9b29e0779dcca44e82199761863644e91`  
		Last Modified: Fri, 07 Feb 2025 01:55:03 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa3618f866837800ad57019fc7f1e55de79be96af72203ae171e982aac01fbc`  
		Last Modified: Fri, 07 Feb 2025 01:55:03 GMT  
		Size: 740.4 KB (740356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63e3d5c7d5e862212462649ece54244ca075f53a22e1ecf30252045c2446838`  
		Last Modified: Fri, 07 Feb 2025 01:55:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3448d29d83e51a940bd0c59a4cb56835efa36b9b50d0d52c2dc3d199230d8b`  
		Last Modified: Fri, 07 Feb 2025 02:05:14 GMT  
		Size: 21.5 MB (21479496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:834fb468ebef129eb4e105164d5358da65d52bfa1b6a7f32f11398988e65d8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42eee79cdc2776c52791d898df460de0e2d1d01cefff09228a3f2fa229d8352`

```dockerfile
```

-	Layers:
	-	`sha256:1f6144f2744ac98b34bf0320de2ca3630f6f18f81517abfc1641bdab7c979ff1`  
		Last Modified: Fri, 07 Feb 2025 02:05:13 GMT  
		Size: 6.5 MB (6495771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9852e8ed3afff4c81d1a871465511e2dc4f6d83a094bc2608082b76b8681a2d`  
		Last Modified: Fri, 07 Feb 2025 02:05:12 GMT  
		Size: 32.3 KB (32277 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:312b4626337233e439044f2e85298e1d22172de50222e85f8234b8276e23588c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187573792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b195200d3fbee328653393edac207aeb61c0b318fd354686ebb09ff575a6e22f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 17:19:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
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
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2717552e294154609fe000cd2e7db62a94ef4462e55af20ef755d18586451417`  
		Last Modified: Tue, 04 Feb 2025 04:36:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0d8372a7985947955179add5556c2bd14ac899f883d33bd8b3db0483f89675`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 92.5 MB (92521560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f692565df0252f74a3ec3c3972f36cefe655b126fe86c36fffdb821eaad777`  
		Last Modified: Tue, 04 Feb 2025 04:36:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff937e0da068ad4c3d13b60643b0b1b312fa5686ef4df9a348f19894e3f548d`  
		Last Modified: Tue, 04 Feb 2025 04:37:00 GMT  
		Size: 12.6 MB (12647108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d891cbcabd2c7dfdd29bd366911bdae24ce33a6ff5e0b707bb8604fbec7f30`  
		Last Modified: Tue, 04 Feb 2025 04:37:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f013f730923e576680e97b0f7fcc20048d89a221a6d4ce0164fe174c04f8f7a5`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 27.0 MB (27020877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3d688084794978733611f2fb061181f78a14fb2fae3825a8b01babe96f9cc9`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f18769da1b3e05e1e04f8e1f721d08352886d3e00bfc39d8aee3267542a80`  
		Last Modified: Tue, 04 Feb 2025 04:37:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e95abb148f506d35cbb47b6a27582f6a35cb1c01915f98e41e05d105f72843`  
		Last Modified: Tue, 04 Feb 2025 04:37:02 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155c2a74390d6b2b4011dafb4ad5c579f187ec2ad87d1e5394eebd55214fad1`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 2.0 MB (1972110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fc3a22c246fcfdd29d79943f29284af6a2bd493524ef4f0f083794e26fabc2`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce90e57696e2bb1081707707fa51c6715dd497d094f280fe308982896d1d014`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0318e1732e7f8e0994eb7ca9fd57a47e989d5e4a19f069a3e64f0d259b717`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f34b74343c3dda161d0f5db68c343709fbbd0dcc62916b40ed82d6317e5b14`  
		Last Modified: Fri, 07 Feb 2025 00:29:41 GMT  
		Size: 21.5 MB (21479636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:195a5a8d0a7bd2d57c84683c96cfddea7d939734b9e94c25de1f36ffec2380c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621e6afb1e2ca788ece71fc58ec284abe189a56058ab45509c757d5c5f3ab76a`

```dockerfile
```

-	Layers:
	-	`sha256:acbf08373b40fd7564583757d775efef5fb0a8f11c77d7d844f715189511be30`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 6.5 MB (6473516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6a50d94715859753c3172cebb9db0bb00f06de160b3bdc9c6fcf3f67c64d9e`  
		Last Modified: Fri, 07 Feb 2025 00:29:40 GMT  
		Size: 34.2 KB (34237 bytes)  
		MIME: application/vnd.in-toto+json
