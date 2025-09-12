## `drupal:php8.3-fpm-trixie`

```console
$ docker pull drupal@sha256:f28caef6433dae4e26ae64f0bd6e2664d350754e730fd518a846d66849a1a2ac
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

### `drupal:php8.3-fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:36e575e51c4b96c14bbd2fdc8783e022c7586eeb6a75fb636e84ec94c899fc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195153811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5618eb1dba95fc6a7fe2e9c510d6798c2b776f64d1d33ad82b0ef869334ab2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436dd6a4e0df2f6f99442f95627769e29be264803069601602a8717ef1cee2a`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf577e05081f5219d270419b699e5d5a11daa891626a9c71edeff4dfbda4f1`  
		Last Modified: Mon, 08 Sep 2025 21:46:08 GMT  
		Size: 117.8 MB (117836402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c41c4b65cd3b5ed6f9d7c2330f92a3c0201c8570ba5454cc1113280856e992`  
		Last Modified: Mon, 08 Sep 2025 21:45:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedace43d9fe59159008d52231f3af49c4ee1feede95cf172c10b15bff3c17e`  
		Last Modified: Mon, 08 Sep 2025 21:45:52 GMT  
		Size: 12.7 MB (12731010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21a6390c6b4f338547642090a57f97740bfe2f82e2d4562827281e60ccd007`  
		Last Modified: Mon, 08 Sep 2025 21:45:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca112d35ba6e81f8e4ab5c209c817e82d2bf44319ca333342b2b8b9c4250b3c`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 11.9 MB (11892967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7d791e20ad100274137f081f763787ad9869d338da110da9f7b45dd93896af`  
		Last Modified: Mon, 08 Sep 2025 21:45:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a9b8def36b84357ba2d08d56d709be0642b3477e7f79b39c643db9bd09a83`  
		Last Modified: Mon, 08 Sep 2025 21:45:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f8011a0b6b4b2b559f6a07bf2ed7be106051508a3bb2916f5a323580b8bea6`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25089592a83257371648a3411054a7439e2fa2b97a477e81433a663f5e3e1ec1`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83259f46570bc3f375344100e4922bdf06f80a01a81ff76c6e641063be2157fb`  
		Last Modified: Mon, 08 Sep 2025 22:34:59 GMT  
		Size: 1.6 MB (1619945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d003c0cee8f1393062b91f80195d8f89a00e59655aa844f6d34f2063b42679de`  
		Last Modified: Mon, 08 Sep 2025 22:35:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45563a4b9491e4f9939c6cd7622a3b5f7956ebff45273278c11337e8646da1c7`  
		Last Modified: Mon, 08 Sep 2025 22:34:58 GMT  
		Size: 751.2 KB (751224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe38dec42b86244956b5c2b6c113090a5d6fb95c8ea2340055e59c7f89ffd28e`  
		Last Modified: Mon, 08 Sep 2025 22:34:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab32d9dbd0591169a0aa1fa820a5b92e616c957180f51e34559975a2691f49eb`  
		Last Modified: Tue, 09 Sep 2025 03:05:26 GMT  
		Size: 20.5 MB (20535244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:25ef2591333d223d80fdf68683c956415a07b5bc8413310b50a059aec33bb0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0f230bcde5e896e524b233f126fc52ee44bad47285037672532b7b3474dae3`

```dockerfile
```

-	Layers:
	-	`sha256:3643e89872f4e9f3d58b3a880f3de9b641bed3cbdb1b12c1587e84bdf4ad6717`  
		Last Modified: Mon, 08 Sep 2025 23:03:42 GMT  
		Size: 6.8 MB (6810419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:335ae59655e1ba83c180668f841753a0275b0532bf0771e1e5d5f3d79a2f3578`  
		Last Modified: Mon, 08 Sep 2025 23:03:43 GMT  
		Size: 35.9 KB (35901 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:e9cdc2c7ebf8ddd624bb7e0dfe5be635c8e9f131aa93b86f0a5c68a31848f713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157891461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2534c448015867913e3ba5f895fd1abc16000812197a7216a82dc6d3a4767227`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265835c6b0c6f546efdfa654161b9e25681e872a1640c780e2d4ada1f0e0b6bb`  
		Last Modified: Mon, 08 Sep 2025 22:15:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f639826548f2d17c437e56cae04907d144132bcbb7726112da73b31bd2561ca`  
		Last Modified: Mon, 08 Sep 2025 23:25:30 GMT  
		Size: 86.2 MB (86244526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1070c22314e8ef77db96b0bc805e71dce9fb19ee317b7688a2169b81f87ac247`  
		Last Modified: Mon, 08 Sep 2025 22:15:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88b023fcae499f92caf765633494dcc54e853d28152579443194836da4ac5f3`  
		Last Modified: Mon, 08 Sep 2025 23:22:53 GMT  
		Size: 12.7 MB (12728310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff382156af9474d0ee10538cb07bbba906e989bb836a86daeb14422ba726a8`  
		Last Modified: Mon, 08 Sep 2025 22:23:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8238ec96415e423f1dae0294745c74454768eab53c7faefe0c1726dfb4ec48f2`  
		Last Modified: Mon, 08 Sep 2025 23:22:04 GMT  
		Size: 10.1 MB (10074944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce02f5d8dcbaf53d9d7c01722a2090a147952f887b6b6a6b869662cbf16b86b8`  
		Last Modified: Mon, 08 Sep 2025 22:23:50 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44783ea4549e4cbf178e9d42e75105b7a9f4e21d48d510b87718b3c1e120c686`  
		Last Modified: Mon, 08 Sep 2025 22:23:49 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c25b0d53e53cbfbc14422736650b6ada7d4a0aaeda15ecb97ab349cf189c7b`  
		Last Modified: Mon, 08 Sep 2025 22:23:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f375205e8adaf75690f266fa182a183da18b17f3051b6e28cf547a20f60c3720`  
		Last Modified: Mon, 08 Sep 2025 22:23:51 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8386364a9acdb91bdd5a6098c47d5dd57e6c2d8c0b0ca90c8c68cd0cbe78810e`  
		Last Modified: Tue, 09 Sep 2025 04:03:28 GMT  
		Size: 1.3 MB (1336215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b92aa09dfbf172d10f3f459ad17c336ddb20a8be702301b9fb9d58ac5c8f2`  
		Last Modified: Tue, 09 Sep 2025 04:03:24 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab7c2513dc8552611eaa0f88942097db6245805e58d19b128960cfd50e5d9f5`  
		Last Modified: Tue, 09 Sep 2025 04:03:24 GMT  
		Size: 751.2 KB (751226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8abc0ae5afd5c31e3fe8bfcf0677977795aa99982ca258a5809771dd5c8fdc1`  
		Last Modified: Tue, 09 Sep 2025 04:03:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f22c5ed47cafe06cd07d218cfbae073260bfeef90c4f747ac6d6a44ebfd02c8`  
		Last Modified: Tue, 09 Sep 2025 14:02:03 GMT  
		Size: 20.5 MB (20534861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:700d681df269dc2b047712acacb526c58f4886ed2a8a0a0eefcf0e0303d5e355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c727a06264da050481249c22d43221a170683917d65a245924ba35ffde3cacd`

```dockerfile
```

-	Layers:
	-	`sha256:bb119f5afe42f5e976b6480aebe1e449a1f1f82ec043a7e7932f6a9f333ca9b5`  
		Last Modified: Tue, 09 Sep 2025 05:03:30 GMT  
		Size: 6.6 MB (6614252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb5ac89e0f52976cbd5856ef3be050fd8236df704ef5c7afbd09453bd5fcaeb`  
		Last Modified: Tue, 09 Sep 2025 05:03:31 GMT  
		Size: 36.1 KB (36056 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:b015a872f48cd623a41735ba03d55bd6148214acc23e4b30ab51a68b91bfcdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187826601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6ee266453c0d9422c0139357aeb5a8ac44fabf9fdc002ecfc723167575b8f3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56472f244d24bcddb9bd8a869ed129836a40d718c88024df80e2cc2902f5694`  
		Last Modified: Mon, 08 Sep 2025 21:38:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a546e2d572e4d566ff11d3f7406cb6f36910f4c5ba8d16db307a0ec6da0350a1`  
		Last Modified: Mon, 08 Sep 2025 22:08:32 GMT  
		Size: 110.2 MB (110161321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e834a6359d4ae542425d05f22211a9d22d69cb37efd62bfeaad1c571cc8519f`  
		Last Modified: Mon, 08 Sep 2025 21:38:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e7e21a01396cee69fe0ab5eaf6e3e1e27da02c196a892f100dd4f450ec6094`  
		Last Modified: Mon, 08 Sep 2025 23:13:10 GMT  
		Size: 12.7 MB (12730549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c01be5f45b6bdccbbc30f13e268dcc7bb2d19fa18be92a36e3bb4f80138c33`  
		Last Modified: Mon, 08 Sep 2025 22:12:58 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05e53817576285ed84096289e7adea08775d214d95c341491020368da1df3c9`  
		Last Modified: Mon, 08 Sep 2025 23:13:12 GMT  
		Size: 11.9 MB (11920257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e789748347d6e8522741c89b72121ff9eade32b7b5cc7b1e75a1be4ba8d281`  
		Last Modified: Mon, 08 Sep 2025 22:12:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd1a1ed6d117e2c96441063c58278ded4fd960601a23b035edd1204441b491c`  
		Last Modified: Mon, 08 Sep 2025 22:12:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e54b0b62829289989dd20c4e06ac3da3cebadb438e70b71c324845144a8273`  
		Last Modified: Mon, 08 Sep 2025 22:12:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb2dbb3606d065fd920f56961c7828cbfb51ef3f8437cf99d3dc601392dc566`  
		Last Modified: Mon, 08 Sep 2025 22:12:57 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f630e6f8966d52051de736d6dd22433a8c13ebe518fc0a68b2e7a6d41c8a1a3`  
		Last Modified: Tue, 09 Sep 2025 03:15:16 GMT  
		Size: 1.6 MB (1578029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490c30d06e4e3b482e0b24d5e5732d191c88b98bcb6f0964ebe6a22ed07ce576`  
		Last Modified: Tue, 09 Sep 2025 03:15:17 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a0ef783f3e55bd2f2658511d4f876ded9c93c65117b0dc7cddfaa3d7ac224b`  
		Last Modified: Tue, 09 Sep 2025 03:15:16 GMT  
		Size: 751.2 KB (751225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafe547ab0d116fdebfb687a083374f3df30f16f1f491822422ea227f1aae3fb`  
		Last Modified: Tue, 09 Sep 2025 02:09:16 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a96a313a368fa54c3ac6238888c463d926f7b6a442aa2c9441e6e271c3efaa6`  
		Last Modified: Tue, 09 Sep 2025 14:02:02 GMT  
		Size: 20.5 MB (20535061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:daa72ccdcb98d1b50cb9f24540f86370280db31827630cffe2ba20e6cc7fa294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6943863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbc4e3bc242c814d8b9d4bee57aaf7f5e99ae39b2d7ff107030f5e021152051`

```dockerfile
```

-	Layers:
	-	`sha256:2354f8079486b452c199a26146fecd72b05098dbeebe8342763d09cc57713dcd`  
		Last Modified: Tue, 09 Sep 2025 05:03:36 GMT  
		Size: 6.9 MB (6907753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3108409220e60297ffd980ec8042fdc7878a475e6e35c4c1c24685b9c23d824b`  
		Last Modified: Tue, 09 Sep 2025 05:03:37 GMT  
		Size: 36.1 KB (36110 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:2b3dff6927217c0c4200dcfdd8c8c4b28bc12bdeb1f0885129a02f060cfcdc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195256253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed36e33cb4c36d13d3a790677ec9a5dec6295d8c40ab4635e74f0e09d99fc623`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb1a85bcd6a5486319129d79e6b34689bf0d02eed0ab059f7ddbfc320fae83`  
		Last Modified: Mon, 08 Sep 2025 21:45:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52d6e4e46502ee7bf77b83b034c831af3cd79100f1c10f774bdf56fb360bf24`  
		Last Modified: Mon, 08 Sep 2025 21:45:41 GMT  
		Size: 116.1 MB (116136866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3282a99898d927542250573c23960388f470cc9d86acdeb03d64c01dfb0d36`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc737b98d8f4f950bbfde9b1c04569ad139abe5ef8bef33b51cb1add67fe6416`  
		Last Modified: Mon, 08 Sep 2025 21:45:33 GMT  
		Size: 12.7 MB (12729789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d817f2f1d066b0ca38ae9573cc9188e6193369cf917a9ef51eaa934ae8e0c9`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204756c70348f622c10b5fe360dafa995e75001761229985b6f4c66c1a4e08c`  
		Last Modified: Mon, 08 Sep 2025 21:45:33 GMT  
		Size: 12.1 MB (12101800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29417b0ca59b4aab990b04368959b225151b4f923eb9c8d16d11d2768a4287f`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba3ea6c953d4243a6d57459f71355e8461985cbb1c25a32723aaecc8d55a2e8`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946224565597860c28913fffbc7bae3fe1df409e32f852413f5e68b44b6431aa`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d441bc2d6825d7c76942ce3a6e8aed1c79caa1c04c4d98453ca589f9d58919a`  
		Last Modified: Mon, 08 Sep 2025 21:45:32 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b43a11db4877950f9ea2070865e0d3ce3c486e1bcba9e604d922ef7b6a3942`  
		Last Modified: Tue, 09 Sep 2025 12:13:44 GMT  
		Size: 1.7 MB (1698661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34df9e6bd117aaaa3a9a5bc2439b8e0c304a41a0af83ee7bc8d87478d50f5666`  
		Last Modified: Tue, 09 Sep 2025 12:13:38 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e24f9787d48217d606b33dd9038d27bfbca30516b95c4faa7c759ce909f0fa`  
		Last Modified: Tue, 09 Sep 2025 12:13:36 GMT  
		Size: 751.2 KB (751223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afd83c90912f434e78036914adcea526088478a74a8e9f6d88ab451febd61ea`  
		Last Modified: Mon, 08 Sep 2025 22:51:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb207055917f833ee8bbebb2d4b9fe0da4971f2c9c608191b6318dacc2fb393a`  
		Last Modified: Tue, 09 Sep 2025 12:13:02 GMT  
		Size: 20.5 MB (20534600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:05043b2c90c8bc6962158b92d89210650679f6a567cfe16ca02e35037f9f2886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6820122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154eda200314cec9c9c1e48b75baef5a72d00f4e609e27cd1ec41e75f8bc06a1`

```dockerfile
```

-	Layers:
	-	`sha256:e90831080e4888ca47ba392dce8c7daa4c8ae00fb0522c805e2a8596cdb06793`  
		Last Modified: Mon, 08 Sep 2025 23:04:01 GMT  
		Size: 6.8 MB (6784283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259b7c052304f8fb07e066a1f9d0a097e6830d2e14151cab25a89cd104f70dde`  
		Last Modified: Mon, 08 Sep 2025 23:04:02 GMT  
		Size: 35.8 KB (35839 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:c3ec8946b0aaea6a76ee2a4dd3a4031c5bcfac56a90ba6b84a9a8b03a14e5102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191464697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e68ce5b77f88905a493ca8ddd4f7a45eb3fb749d8959c3599feffc52342097`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8eccafbdf06ecb6a7d419e820836d964e71cf25b828dec52e259f312c37d18`  
		Last Modified: Tue, 09 Sep 2025 08:03:42 GMT  
		Size: 12.7 MB (12729917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2830b1373986247fdb37551e61a893d6ac0e924ac25f5b2794957ae44093ed`  
		Last Modified: Mon, 08 Sep 2025 23:47:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60317dd4fa2149cf337ce6470a2d06e9597ee8e31dbb7b875d8a84975c8fa33a`  
		Last Modified: Tue, 09 Sep 2025 08:03:47 GMT  
		Size: 12.4 MB (12434097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9de00f8074d723b4b69952ad5185f82bea5ca4b57c2b68e40f8eb813b8e42`  
		Last Modified: Mon, 08 Sep 2025 23:51:43 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300de6277fb5a32c0047f17c8d891c793183869e07f21081368a9c6b5eb2dca1`  
		Last Modified: Mon, 08 Sep 2025 23:51:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2b83d1d8c0d0dfd5c82220cae1b823f7b5b8c3a9387ebc4dbccf294ea9d59`  
		Last Modified: Mon, 08 Sep 2025 23:51:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb877c8064b47ec5d96f538d7971e9e1b2cba79dd6d09382e7f7053a953555`  
		Last Modified: Mon, 08 Sep 2025 23:51:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735ef551736cb8e8316a16e1b02f724f049a2583e2a88dbbabe0795056ba81f0`  
		Last Modified: Tue, 09 Sep 2025 16:35:42 GMT  
		Size: 1.8 MB (1809693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a96a954843ce2a7e93c1433e7bbc7b54a4163835b00a67b38a90a19f2cdfb36`  
		Last Modified: Tue, 09 Sep 2025 16:35:42 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06434a563d019a5d4429909993a82d31fe9aa831368c9cab49b22f2a5840a3f`  
		Last Modified: Tue, 09 Sep 2025 16:35:42 GMT  
		Size: 751.2 KB (751226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91808f192a9d86e664e3529d5657ec9980beeeba54b1d0475d32decf49eb0caa`  
		Last Modified: Tue, 09 Sep 2025 16:35:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640c353d6230aeecc1c0cf9749a3645cdbd8773ee34221e5f9399686a5a1e9f0`  
		Last Modified: Tue, 09 Sep 2025 15:43:41 GMT  
		Size: 20.5 MB (20535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:7d584980f041c58bef94065c226dd5b306d936a706ddc558f8909ec1c1a61d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de9a513ef4a9a0b79c2b7eb242153e2ba1cc06b75dc8b55961f09e251b7dfee`

```dockerfile
```

-	Layers:
	-	`sha256:74689c7580e6a58ba4c5d2f59aa30602ff0debd30a50e658ffcd069bd3a11fd1`  
		Last Modified: Tue, 09 Sep 2025 16:59:06 GMT  
		Size: 6.8 MB (6810156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f4de887a1ceb6309ae442ea130b4eee568e6368ecb885c04623dfc2b2b933c`  
		Last Modified: Tue, 09 Sep 2025 16:59:08 GMT  
		Size: 36.0 KB (35984 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:4f988c5f7d6fba77107e121226a585bbd3ffb998aef9c85ba83847927fd0e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221886001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741cf863efa74f98f1b2a6e9b39f87deeccd5241eac903737fd6f2783f1f590b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae3e77da310b8f6abd1c47c2c908b688364ff453788dffc1ea3755bda9a618`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25a2ea3673eda57f8891f3fdc7a2b5bd7baa28ce076ff3427218ba02258d5f`  
		Last Modified: Tue, 09 Sep 2025 20:58:30 GMT  
		Size: 146.6 MB (146579169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd9eb164bef808ab9cc8b8afd7d2a60572baa81f3ff4c56c34d90a36945fb1`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d85097f0a6672354a85d93e8c053fcf5d1dd7f6c543d2506686325b7b17f5`  
		Last Modified: Wed, 10 Sep 2025 02:59:58 GMT  
		Size: 12.7 MB (12737431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ab8a99da0b98aa95bd386a59f926b08b6a17c6ea87befcef5b8ecbe50ba37f`  
		Last Modified: Wed, 10 Sep 2025 02:59:57 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba01dbe1ec31af8b6269bb96830e2779bc17cd39d8773ef8ca29cf1954b781c`  
		Last Modified: Wed, 10 Sep 2025 04:51:01 GMT  
		Size: 11.5 MB (11460105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ba3a4def71ba01d983751e45ef62a2faf1d9b9958a66f88106e959e1a3642f`  
		Last Modified: Wed, 10 Sep 2025 04:51:00 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4951d91a7c955fad44bdca01e0602aea28d7d18f42a574460a59790901cff57a`  
		Last Modified: Wed, 10 Sep 2025 04:51:00 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799a9b4fa86d30ebe2af443ff5290719cce3b7bd3674764573d8e9ce2f2b9379`  
		Last Modified: Wed, 10 Sep 2025 04:51:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69883c51832cf8c6685f23539e85f5947733ba4fb36d1c3e0aa42e72be480f54`  
		Last Modified: Wed, 10 Sep 2025 04:51:00 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e990958491f1f9c6137ea4d0d1a4143b068a26e11dcb2b51272174dc10e818`  
		Last Modified: Fri, 12 Sep 2025 03:14:27 GMT  
		Size: 1.5 MB (1537422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e855ef2b9302455887ff0a7c12ddd438f4f78b9e99efd77c46bd573a9fbcf4`  
		Last Modified: Fri, 12 Sep 2025 03:14:27 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b978a82d51536e2e3e8e9ee9396faaf2bd0072818607001461d8624f614eb1d`  
		Last Modified: Fri, 12 Sep 2025 03:14:27 GMT  
		Size: 751.2 KB (751230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646842ac8312169ce22620054035579b0e6a64bf27b868613a2d6c7b4aef6f33`  
		Last Modified: Fri, 12 Sep 2025 03:14:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cd3030efef117ac79606454a79f4b90e8bace0fadfe70fa2d4ce37d4087397`  
		Last Modified: Fri, 12 Sep 2025 03:14:31 GMT  
		Size: 20.5 MB (20535726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:16cb873e5f33e9292a9eee5083d43bab89d5f3483ae3ca22958487272065ca26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6918199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf4d0e9fbe175fb9acd0cccd0d3323d9fabc83b16c14d88fce50b3dfce8e8fb`

```dockerfile
```

-	Layers:
	-	`sha256:d789217629d50665d58ab6d45e841c783aa6d4d9bc545d21e2888df247ff4dc7`  
		Last Modified: Fri, 12 Sep 2025 04:59:09 GMT  
		Size: 6.9 MB (6882217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6def0154b2b92034f0d3d08ed3cd269ea6cf182927d91543eddd62285e09da7`  
		Last Modified: Fri, 12 Sep 2025 04:59:10 GMT  
		Size: 36.0 KB (35982 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:602ffe14fe268e0c9bc064c83949af555368a3cc44de6d0dc6b0b57c9555fae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169826997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf612e5bc1bd7ce29daf2cd2101ebe1d0ebfaff5ff1f00ded98df57b7c6a44`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 28 Aug 2025 15:22:56 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 28 Aug 2025 15:22:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_VERSION=8.3.25
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Thu, 28 Aug 2025 15:22:56 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Aug 2025 15:22:56 GMT
WORKDIR /var/www/html
# Thu, 28 Aug 2025 15:22:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 28 Aug 2025 15:22:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Aug 2025 15:22:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 28 Aug 2025 15:22:56 GMT
CMD ["php-fpm"]
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV DRUPAL_VERSION=11.2.4
# Thu, 04 Sep 2025 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fdcf952479041c13f882278c495e7bc45a0f5fa2c0729458fca6bba80e078c`  
		Last Modified: Tue, 09 Sep 2025 02:16:43 GMT  
		Size: 12.7 MB (12729027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a0aa90f838f11dfb678bde6425513970293a5aca8dd1a77f8749fdd3f7c013`  
		Last Modified: Mon, 08 Sep 2025 22:51:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4102b4e3b5fa252ca88118b9635a5747080d0eb72f5d79ec35e0d618673590b5`  
		Last Modified: Tue, 09 Sep 2025 08:04:19 GMT  
		Size: 11.8 MB (11763249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293c2277a5385f5dc2bdf6fb11642c4f38b260015a87643415335d79237576f1`  
		Last Modified: Mon, 08 Sep 2025 23:34:10 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b7aed5c8660e5dd515bed6379b63defd9d006c6ba9b9112df044d4f557f96a`  
		Last Modified: Mon, 08 Sep 2025 23:34:09 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222870cb9f0286fc4be7625dec927876968d3563db00c695db258f54d3a028c9`  
		Last Modified: Mon, 08 Sep 2025 23:34:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee275da8106de833b45753e30c2dfc7f16f5e03fde38d4ac61fa17c9b2b90f`  
		Last Modified: Mon, 08 Sep 2025 23:34:09 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50a95d8eef25ec0768221e2d1ed271063fa60a73223d69c5377aa8ff3a29f74`  
		Last Modified: Tue, 09 Sep 2025 11:56:37 GMT  
		Size: 1.6 MB (1639176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc59c11a220bd56067e31dd5d2895d306912e484c8ff47954957100dec7952`  
		Last Modified: Tue, 09 Sep 2025 11:56:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494cb97145e18d5303837f67b81476e178845522b04c81478c010a027e2842b4`  
		Last Modified: Tue, 09 Sep 2025 11:56:37 GMT  
		Size: 751.2 KB (751224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71247d6c6649a5702d3ac3f2a04eaa2ad0a6c6f228f39b71e694e0c212d84abb`  
		Last Modified: Tue, 09 Sep 2025 11:56:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe588d1d0ac61a5e1849e1f75089a83a16f91e33514bad10b0bed08d7e829792`  
		Last Modified: Tue, 09 Sep 2025 11:56:41 GMT  
		Size: 20.5 MB (20535370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:4e9661d52a8c582dee57e3ad21349a148e5c5c042523f11417963f21056409ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6663581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8323a2664950c0b4aa08e7b2b998f17e9aa7324d8f260119f6cad28737732181`

```dockerfile
```

-	Layers:
	-	`sha256:dd4fbbe761fbbc8a1ef2b6f95476d54463e1c1e15cc7f6b7233fdf45c1e3306f`  
		Last Modified: Tue, 09 Sep 2025 14:02:17 GMT  
		Size: 6.6 MB (6627685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5f36b56fb7ac48ed053b180ea9a306832db75db0dab9c094ec382e49f1b5a8b`  
		Last Modified: Tue, 09 Sep 2025 14:02:18 GMT  
		Size: 35.9 KB (35896 bytes)  
		MIME: application/vnd.in-toto+json
