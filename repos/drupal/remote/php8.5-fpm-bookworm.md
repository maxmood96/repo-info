## `drupal:php8.5-fpm-bookworm`

```console
$ docker pull drupal@sha256:389d8096529280b7c233fb9e6022cd683689fe46573a186e7143fc6a7ca928c4
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

### `drupal:php8.5-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:a0ee18aee2b64be2b748d7896912e2b5622ebba79b494727cb8514e87a1ccba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202034489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7583c043f35b868e013c79b9d2228e63f462a44a6f8c51a0dcd05242815cfa02`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:06:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:06:42 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:06:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:06:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:09:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:09:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:09:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:09:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:09:36 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:09:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:09:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:09:36 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:09:36 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:11:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:39 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:39 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:11:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:11:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df5f98e92fd22fc66921726345841cdadc1d0207bbbbea3726a53310921e73`  
		Last Modified: Tue, 19 May 2026 23:09:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7805adc7151e6cf81f18e08c3b003a106cbe54ca3fb3bfe4f6bbb2b7af607d3d`  
		Last Modified: Tue, 19 May 2026 23:09:59 GMT  
		Size: 104.3 MB (104342099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e7dbc0db1308cfd73f68b3204c8bc69c207f62e149ab6726ea794d0221bbf`  
		Last Modified: Tue, 19 May 2026 23:09:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dff213c36dfa6171d2aa05a9ee30a1ecd00f10cfe8907df3c4b1e7fbe80d4f`  
		Last Modified: Tue, 19 May 2026 23:09:56 GMT  
		Size: 14.5 MB (14503362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e799822f19e2475455f13ed2d4cfb8953c47a57f55268ef04eeed0387e7819`  
		Last Modified: Tue, 19 May 2026 23:09:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fdff8b09e3c7ab7962246fbc29a70272347befad19177a447531a049dfc21e`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 31.2 MB (31190068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb49050e96a6fdc9f37e3d44edbf40dce39dee72995797487f4a40fc356a6f5`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb66b306007f1b475cf09839f25a26db3280d656a21d0e11fae2e7bfbfdee0b0`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ebfe2907fb1006505caf99105fd3593d49b9050cf9da984ad7b21435306d5`  
		Last Modified: Tue, 19 May 2026 23:09:59 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7b38a6d4cd3115dcfd91e2464612b3b1b40db26ffd7eccce25d8f1e70d21e0`  
		Last Modified: Thu, 28 May 2026 22:12:00 GMT  
		Size: 1.6 MB (1552313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ab11bbe2b0ae4b345287288925c15426daab4fad882904bf9e70ae61f2d33b`  
		Last Modified: Thu, 28 May 2026 22:11:59 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b02df3ffa545771f942d425aeffc10bdef0e4fd4f36f5f3153c8347b66aae9d`  
		Last Modified: Thu, 28 May 2026 22:12:00 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398858e505ecc59316fd8b95f4bceba5a2d6989abae69a6cb82e4a23043f8c47`  
		Last Modified: Thu, 28 May 2026 22:12:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e82cca56eb28efe22576e7d1adb390f2642048f647eea090acd7521336875a3`  
		Last Modified: Thu, 28 May 2026 22:12:01 GMT  
		Size: 21.4 MB (21377220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:288d1b17506466b281a16cb7e86672b61d07f32ad9d6281a81cf181576c8eccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6555381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caa9407a08e5dcec04bc9851c99d0e0b06f57bc7deabbd713b40b9076caa255`

```dockerfile
```

-	Layers:
	-	`sha256:198d539cfe5da45ad6d435224a08c00e0dcba7a4fdd8b1339823c0dd5cb02ae8`  
		Last Modified: Thu, 28 May 2026 22:12:00 GMT  
		Size: 6.5 MB (6521836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ff0997c5128fcc83286f56de9707df54824c45cde9f5bf05faa30703c7f1b0`  
		Last Modified: Thu, 28 May 2026 22:11:59 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:246d2938671e5228903ac149d80b6250e194c316e1e01e9962f24060006f543d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165941118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dfa574edfaa9a325a501ddbe4078af24e27e076092f6bfad84ad7c5309fa16`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:10:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:11:05 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:11:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:13:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:13:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:13:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:13:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:13:51 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:13:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:13:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:13:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:13:51 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:15:08 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:15:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:15:08 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:15:08 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:15:08 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:15:08 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:15:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:15:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f63546be9c0f89fabd8fdca3ee94d5f336f15f1c2c13c28151021f917f0af`  
		Last Modified: Tue, 19 May 2026 23:14:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7a6c6c756ce89788457e518a02b65d2bf5313bf36114c13e8ed2aa766761b`  
		Last Modified: Tue, 19 May 2026 23:14:09 GMT  
		Size: 76.2 MB (76154861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba60e347541cd683b62e3ec7596369a8f28398e0bfa4d4c5d1600242878561`  
		Last Modified: Tue, 19 May 2026 23:14:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025045aeb0e1b7a061e5b72fbee107c9b8f21bf4fdf49f76d5b465ad1cd2097b`  
		Last Modified: Tue, 19 May 2026 23:14:07 GMT  
		Size: 14.5 MB (14501473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b224d879f1e3b331fff7dc95a879a3575434f9d26854d6a910aff31a67f6c3`  
		Last Modified: Tue, 19 May 2026 23:14:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db087c6b91a66c4f8a838534e8cba1994c771fae8ea01f0c1793802ab2a0f36`  
		Last Modified: Tue, 19 May 2026 23:14:09 GMT  
		Size: 27.9 MB (27858047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6534887f17c9f84bea9240f5924b1ba0de41575946cce9d73f7f590f27a06d`  
		Last Modified: Tue, 19 May 2026 23:14:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1d13c2c6929e87089c89c80aecd1e0ef33e5ca8c33304d13fd369ee7a9544c`  
		Last Modified: Tue, 19 May 2026 23:14:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc611d62c640d13d2336597c6da8c6d9d2b9392e3f4c986120c4bd1b7fbed4`  
		Last Modified: Tue, 19 May 2026 23:14:10 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31dc8626d4a3b8eb4a0dd80e19912b3f7da9a72144e7edc4c97bf65fb6a323`  
		Last Modified: Thu, 28 May 2026 22:15:33 GMT  
		Size: 1.3 MB (1272056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706893ee488e85e078529b29269869ae91faf1b41a2ad4f3e5c2884f891fbf18`  
		Last Modified: Thu, 28 May 2026 22:15:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288669ca945c4959ea10b630aa375f09e65902b3d39129e03f58f684c9107138`  
		Last Modified: Thu, 28 May 2026 22:15:33 GMT  
		Size: 822.5 KB (822520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce563afd8e07671ace3c398013a8caf8d0f3e0ae144c683a150875d907732c49`  
		Last Modified: Thu, 28 May 2026 22:15:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735a4064a1eef83d290c2286946f0a0d6225184a63310767f6c71a294ceb4194`  
		Last Modified: Thu, 28 May 2026 22:15:34 GMT  
		Size: 21.4 MB (21377156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f6b3d7bf841eb82c87055a8376aab9e528805f2fb65b9fb27c8e359ee4160d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6368790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ae25d5efaf8f5caafe1a16e070ba34b88c4a7555809c760c6892e0d1c2495`

```dockerfile
```

-	Layers:
	-	`sha256:dda3c75a69b768568f098b6d9b91777bdbf811620d974032fd1b50ce174f6a67`  
		Last Modified: Thu, 28 May 2026 22:15:33 GMT  
		Size: 6.3 MB (6335124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a34d92338b64a7aca9775780c016332ed35b74398bfdffadd8f67e5e302662f`  
		Last Modified: Thu, 28 May 2026 22:15:32 GMT  
		Size: 33.7 KB (33666 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:04477c6571698ad39674d2034903144d755465edae4a1f794f12510c34018302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195271081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5db5b2c0db3b092ca0b9ead6835541bde96f83a0fd73ecbc4388dd675e850f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:06:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:06:44 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:06:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:06:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:10:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:10:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:10:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:10:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:10:01 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:10:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:10:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:10:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:10:01 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:11:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:48 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:48 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:11:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:11:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95888a7161294a89b47860f8ea570f965b909716b5234a7b24a4d0ee279a8e48`  
		Last Modified: Tue, 19 May 2026 23:10:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552724b598cd6ce8058c9ba595053a01e2a09fdd222e7ea1091ae1e490d37f49`  
		Last Modified: Tue, 19 May 2026 23:10:23 GMT  
		Size: 98.2 MB (98174507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6662bb4bb84462b4502bb59b3a30546a3e307dcb9004b6ede29bcf88fff12299`  
		Last Modified: Tue, 19 May 2026 23:10:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb341b734bc417e04730f6ca89ca56374f9bb339887b40fb1779e19dc67df0c`  
		Last Modified: Tue, 19 May 2026 23:10:21 GMT  
		Size: 14.5 MB (14503133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a940039dbf0aee1227f68de1faa78b6684418952aa22cc8550247c7478c8cfa`  
		Last Modified: Tue, 19 May 2026 23:10:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869a3c437de557937cd1b9b657c427bb90871d0623afd9a18737da886b644ea4`  
		Last Modified: Tue, 19 May 2026 23:10:23 GMT  
		Size: 30.7 MB (30725443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e004d5dd4466306b02cd58eb7765091f0e31945144209c4e1f6a01efb77e39`  
		Last Modified: Tue, 19 May 2026 23:10:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4418e481fb9dd840228ef0c56a2a51013f087afdab24cf3f514c89697c050342`  
		Last Modified: Tue, 19 May 2026 23:10:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1219c4eca9a7165f1f7dd4f41b43bc38dc70d80d67f89c463ae621d790f46b`  
		Last Modified: Tue, 19 May 2026 23:10:24 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5556e792519c011929f5c8e148af87a485ea6dc5fdda1654ee104cc248428a`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 1.5 MB (1539903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e005102b9c7086d8b481fa7dd51f8df0cae088e34cdc8d7550d68ad8606c0d`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9540e7d954cbfe1b0f200141441d2064977e7531ca02d1cb556b7df7af4fb106`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e606bd580ad9d4b81b7cab4fb676a9b2096077487b75cf402b89ff7466482a7b`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa009455122c3181971d4826a8131ae612507b18910180bfc05c03836664f39c`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 21.4 MB (21377166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:73c0a0807ca2053cfabb3ebbab21213fd0d18c15b9b95b172ef35791e862fa5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77f12970c4011ddbb5173a9a1584473c8e643286b4c343a39e0cbce65f833fb`

```dockerfile
```

-	Layers:
	-	`sha256:a5fc3c90a558d6cab2b537e75381cae063952206f012584297891a9b7441dde8`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 6.6 MB (6550233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e593deaea2dfa23b5d01c5e8e166e2c0061769a11002c204ac80172c908e95`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 33.7 KB (33699 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:3543ade5edaa3c98888494bf849f9bbce42447a1b89840c04b0d961b1e929fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200898157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f185a164d473f66807494ff7a21e25dd290e2b39d76ee3cfe1a26e4b35e97a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:00:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:01:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:01:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:01:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:01:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:01:07 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:01:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:04:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:04:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:04:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:04:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:04:02 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:04:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:04:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:04:02 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:04:02 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:11:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:48 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:48 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:11:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:11:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39820718915dcf151b4bd650833e0f10f2288ad80c64f4584cab09269067e0b`  
		Last Modified: Tue, 19 May 2026 23:04:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f68a943c2531b5ad6eb981c3c53923b5c90ac1925526463a91b83161fda237`  
		Last Modified: Tue, 19 May 2026 23:04:24 GMT  
		Size: 101.5 MB (101535731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e7dcb157e4b52eb1cb144c0e65a3cd85d2c1df31e725c1c2e9eef8bff2e883`  
		Last Modified: Tue, 19 May 2026 23:04:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa59de873867ab2e506db5eb384c387bcf5a153d129d86824c3b41cc0a74456`  
		Last Modified: Tue, 19 May 2026 23:04:21 GMT  
		Size: 14.5 MB (14502494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f8b92672f17bae92cfb04c587599fede4998f81c782edb84e47a71e153909`  
		Last Modified: Tue, 19 May 2026 23:04:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2198b5ba2ab838138fade85d3558f5e035b4d586033cb7f1b4b44dd6762dd36`  
		Last Modified: Tue, 19 May 2026 23:04:23 GMT  
		Size: 31.8 MB (31803419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501091e927d47fc590cbf9e3e08487c860308b263d0f1027b772bd67473d2037`  
		Last Modified: Tue, 19 May 2026 23:04:23 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be489881d6cd73f56e9b62e574056741e5290f7faa6cf6b6adcb909a75bb534c`  
		Last Modified: Tue, 19 May 2026 23:04:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a291788f78b3780e1ef8cd1210d837d8dc3934be787a097e823e93635e0ed38e`  
		Last Modified: Tue, 19 May 2026 23:04:24 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57702e842d188dd208e4809713a738131dc44d44d32fc770e5ad060ed39dda67`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 1.6 MB (1624950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0e859bd43c139fc50e2fbd324e6697fa00393b70e638ddc5667618840e8db7`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbf15af852bd8de27b8ff3b3bd99fb57fc739a00d1ebb5a5f2a71a05b05e849`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 822.5 KB (822520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e606bd580ad9d4b81b7cab4fb676a9b2096077487b75cf402b89ff7466482a7b`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0405cba4ee5f3bcd85ffad3934c2b59a54d0a70f22f0c63856381a01c4cedc7e`  
		Last Modified: Thu, 28 May 2026 22:12:13 GMT  
		Size: 21.4 MB (21377078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:e14b5440ac7148693d3f582268d619b9746760bed5085b8a79c1f338ed78e899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff89ff2caa7a28b9ae269cb92d059c6352c5b132306d3d93a5ae4a06e00d695`

```dockerfile
```

-	Layers:
	-	`sha256:f2a2af74cb7701f855a39a84ee09b62f0640c341bd339d6e743527eeae2a654c`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 6.5 MB (6501616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0983b0668d4b7c861214717c85fe59d5bf5dbb3d63d62a2eadbc39e85f94fc1d`  
		Last Modified: Thu, 28 May 2026 22:12:11 GMT  
		Size: 33.5 KB (33502 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:9fa76792bfc2ca2f514f1a45ec81632720b0865e3d1b37b18780d3213a7cc882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.7 MB (205730008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060ef335fb3f4d320c97fdbfd45e2436f25e64551d9d370c5d85138f11c70569`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:36:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:37:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:37:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:37:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:37:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:37:20 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:43:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:43:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:47:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:47:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:47:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:47:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:47:15 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:47:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:47:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:47:16 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:47:16 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:13:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:13:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:13:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:13:15 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:13:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:13:15 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:13:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:13:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d67bea8271af9f1a8341d4c4e22bf574471fa182ec2cc739cd09fd119426a4`  
		Last Modified: Tue, 19 May 2026 23:42:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b684ff995db404f0fdc8b8f91054b27675cb85131e4d658452b1d85d5fe8dd`  
		Last Modified: Tue, 19 May 2026 23:42:43 GMT  
		Size: 103.3 MB (103333897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd36feadb89d85491f5bd9df54ddebe07eb22749628d8d2ddbdeef96db30987`  
		Last Modified: Tue, 19 May 2026 23:42:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775b2fa747abb9709f05296fa033292f671207f69a6195d6f0b7101e72b56b9f`  
		Last Modified: Tue, 19 May 2026 23:47:43 GMT  
		Size: 14.5 MB (14502766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f27b0ca2567cec12427aa674627a87fc32ea43db3cfdd6c14985927a65538`  
		Last Modified: Tue, 19 May 2026 23:47:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab652e8486450cb2b987597ce37fe16c17c2138e41d901ca1db66a321ab616d2`  
		Last Modified: Tue, 19 May 2026 23:47:43 GMT  
		Size: 31.9 MB (31853124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25488a285a4235dcd211e42eaedf6707a0792d01410e175c9c7dfdde3ddbcfe`  
		Last Modified: Tue, 19 May 2026 23:47:42 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc3ae4a4e71582a6e7b938364fa442e7db59304a9f2bbe487b28bef0955ccc2`  
		Last Modified: Tue, 19 May 2026 23:47:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48ef68b57f6230bc99bc98a7d05408ce17004bce58ed3c60995750137eb9c2d`  
		Last Modified: Tue, 19 May 2026 23:47:43 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bfb012b6ab986e9ac727d480c4f2ce33a53991f6f49a4cc887242afd3291df`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 1.8 MB (1752970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb7305d31abe730337bdd07915aebf1a7caf56bf2004e2dbc4d9769cc9ee064`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194440e9ce6b16ef8d5f1e1b5d34ce298b966521d791e909593af9af5fa9789`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 822.5 KB (822518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6785138989fc0bb982e8e54d65d99ffc41ed027a7f7fab431a89efeba3c31ab`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82fa52cb62cd0071c4995d0f2a41b9d35e4f4dabd0c8176b550263fe1ee477e`  
		Last Modified: Thu, 28 May 2026 22:14:20 GMT  
		Size: 21.4 MB (21375623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:5f6c2ae9cb82facdc2695504ca8c08a9649ce06c0bb4f3eb9656e0f66806fde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6532163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792fefd703c657fefd1ddd06c7d9914422087d00bc61808620baae990862cd89`

```dockerfile
```

-	Layers:
	-	`sha256:622d069df31fd74bc074f599e00bc5e4b8f83a73139f9f975321f03501942ded`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 6.5 MB (6498560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eba0689da0e3a66f84932015d885cdb65e44081d5f10b5cd12a405c0aee9d3e1`  
		Last Modified: Thu, 28 May 2026 22:14:18 GMT  
		Size: 33.6 KB (33603 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:6f527e299c85ec6b263f233c1752cc127ca9b7d7ba6f594181c7dd58bbaff45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175520307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5047e57ebccea33316a8db33b6dda74ef9604696bcc60c88837de6d4c61de3b6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:10:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:10:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_VERSION=8.5.6
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Tue, 19 May 2026 23:10:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:14:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:14:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:14:49 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:14:49 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:14:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:14:49 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:14:49 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:10:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 22:10:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:10:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:10:27 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:10:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:10:27 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:10:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:10:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ef3f197bfaac386157838c8b884dcf5d1a8f665a6438bf5ba96e0770ce4335`  
		Last Modified: Tue, 19 May 2026 23:15:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7c6f1adb9eba80437e67eb04dd4c5e13162193e24c779758e72facca28269`  
		Last Modified: Tue, 19 May 2026 23:15:18 GMT  
		Size: 80.8 MB (80829888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6ece8af35bbb5e15d994b9c90ba748a6895224d39eecf02bc093a1678a4b0`  
		Last Modified: Tue, 19 May 2026 23:15:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314eb6229a33d6b5d1df19fba01a7c9bfabb5674c70dc42c4ea373fdf6b3869f`  
		Last Modified: Tue, 19 May 2026 23:15:17 GMT  
		Size: 14.5 MB (14501809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fa22840afddb9f6a93f567202e68bcc75341d662db54c002b157548d31ac8f`  
		Last Modified: Tue, 19 May 2026 23:15:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb384b302a4c1b9d56b37a6f956d33b160dce773b3ad7fe3aff835c45a751ee`  
		Last Modified: Tue, 19 May 2026 23:15:18 GMT  
		Size: 29.6 MB (29624515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bda2df99f0834dba651af8d8c185a13c68aa5bccc0f4c755f864c09fa36733`  
		Last Modified: Tue, 19 May 2026 23:15:18 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808adb5e91a6d05bc3156c5cf3768bd11833c360a6e15b9ef5de6b51f929e2f5`  
		Last Modified: Tue, 19 May 2026 23:15:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2390fadcfc967f1f2c7b5d30b6d9ffb6a6f6f8f232e70ff57d1758a421e46c8`  
		Last Modified: Tue, 19 May 2026 23:15:19 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d020f0679174edcd973797b16ec1f0ec306e64544aade68563ba831975ea45`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 1.5 MB (1462358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990293955ab1d2d618d32d26a780458ad17445d2f786a42ddc86a317a51684a`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffdfb96578ff5c1cb0debe2a0c8ff4264fa1332070fe92e1c19311e7e490480`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 822.5 KB (822520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b220729fb72237e7a1260f31e958c3847518bef911a567fa88216822a903c8a2`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0753d266e2c7f0b29f95c6d2d55d9a874a4914e96663f299517258b8566153a4`  
		Last Modified: Thu, 28 May 2026 22:11:04 GMT  
		Size: 21.4 MB (21377250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bd3e3c31c89c4d2c5516167fa8bec7598ec025291a59f4236a4ad170e2c23d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6392593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5d97ec1120844cbd05a200264ebb60e3009af36dac7531b2cab99f267e93d4`

```dockerfile
```

-	Layers:
	-	`sha256:57facf8aad25b1d7ed83adfb293df508d645ec83c8952b6c0ac546059cb219da`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 6.4 MB (6359054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b342a2a591bc9313bbbe102abbafaa8802ef33549920f2b39ba5234fa111fc`  
		Last Modified: Thu, 28 May 2026 22:11:02 GMT  
		Size: 33.5 KB (33539 bytes)  
		MIME: application/vnd.in-toto+json
