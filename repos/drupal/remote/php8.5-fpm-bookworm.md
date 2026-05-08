## `drupal:php8.5-fpm-bookworm`

```console
$ docker pull drupal@sha256:a6f415243cd1354417ad5635b04b44fdb6d6806aec576a64a91e518fba241705
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
$ docker pull drupal@sha256:436fc4008de3f2fafd6b6fa63c7fcb42ee09b20ce28a2eb8251a60ee5a193757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (201976846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2ca5ed0b7d947303b29f336dc16d5ec456f65e4011d9dbac55019f9b321f9a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:41:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:41:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:41:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:53 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:42:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:44:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:44:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:44:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:44:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:44:42 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:44:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:44:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:44:42 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:44:42 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:42:57 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:42:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:57 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:42:57 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:42:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:42:57 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:43:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:43:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c88e84f9cb9805e3d9a9b8b072af517683191bfa0f4f917b63856e501f9907`  
		Last Modified: Fri, 08 May 2026 16:45:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3ac5425162c68d7fa82076765f4cef87eb1567ef23f72bbefc493d7278056c`  
		Last Modified: Fri, 08 May 2026 16:45:09 GMT  
		Size: 104.3 MB (104337352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b732656d71f689c48cabb436a1f1279e107c87bf7b7ea97a0eb1abdf099cb7`  
		Last Modified: Fri, 08 May 2026 16:45:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201a3273a4a318a1aa937315bd43d7cea70a938d5332edb9d43a165f278bd84`  
		Last Modified: Fri, 08 May 2026 16:45:05 GMT  
		Size: 14.5 MB (14503406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f59159df4151f9af571e58a21c49576da0c3ba0a2ba01e304f4c4a9ff36c04`  
		Last Modified: Fri, 08 May 2026 16:45:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591cb4f8d342ce0634e1c955006d595c881057de7b250a0a7ce898d2864c267b`  
		Last Modified: Fri, 08 May 2026 16:45:07 GMT  
		Size: 31.2 MB (31190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77191dd079bedbd3548871541107a5a345bb0b74a1c107ba9d3d994a42a63353`  
		Last Modified: Fri, 08 May 2026 16:45:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00e7c43153b8175fa44a8f325be473963b797dea66ce8fdbcb139711d449e1`  
		Last Modified: Fri, 08 May 2026 16:45:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e5726deacdb300b88b1c28fc7998f4e54d2ce563ef7d95e1de364bce3dfbd`  
		Last Modified: Fri, 08 May 2026 16:45:08 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cf37a336b63c594913108cc11879f52a2b70b6be1ca9bd12bbbd89b88080ed`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 1.6 MB (1552180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812b2d15ef9081793c642b3d21179d03c3703adc669689881796e9ef40ee49b2`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e9527faa68ca2693909b4b3501a6f80265a2605913d38bc8938f6e5823aa99`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4698d826b6f76fa43eac2400c3c2c234977f4e10d5b8365ba715e587fc201a`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9f8eb1b25d7976cd318fd5160e7dc75cc4cf98f4a9c01e71187299ab51c1e`  
		Last Modified: Fri, 08 May 2026 17:43:21 GMT  
		Size: 21.4 MB (21353201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:82dbb2101bfc1fc4c34bae10a91a5a273d3fbc0f2ec345f0a83aa4d09d1f4e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6555332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556100da7138e5b0a869d43ca3f1a478bbd70653bf930ce5544306b9f2181b17`

```dockerfile
```

-	Layers:
	-	`sha256:0cea08d95a50a5b8dfb15ea183ef64e6e8ac57e78376abe55c59513abb839a1e`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 6.5 MB (6521790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f780c7ca7048df136a745d1ed1c42757033ebe38c6e013b518e837a1a801a5`  
		Last Modified: Fri, 08 May 2026 17:43:19 GMT  
		Size: 33.5 KB (33542 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ae87501e17f3fabe19959b531749cc3af449e5e9c0aabdf9573334f0b1d3ff80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165885271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181edc94cfaa659f4464365d96457902eb15c1638ad91476fd80587d62a06dca`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:43:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:44:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:44:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:02 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:44:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:46:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:46:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:46:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:46:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:46:51 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:46:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:46:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:46:51 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:46:51 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:42:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:42:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:42:49 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:42:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:42:49 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:42:56 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f47c7c871dca56b7d0e26ac28f238acb55c7b04385db769302379fde0cfcde3`  
		Last Modified: Fri, 08 May 2026 16:47:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3855cd29729ec5f6405a0c03cc2d99bdb04353aa59d42eb88faaff8b143bfff`  
		Last Modified: Fri, 08 May 2026 16:47:08 GMT  
		Size: 76.2 MB (76156204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5c786cc0f063a7e9719694b91d5de98041b391672ae7832033d0aced5b32b9`  
		Last Modified: Fri, 08 May 2026 16:47:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987102d597e37a7f66497cfb9eddd649cf3cd6901fd218e827678ec06f5982b`  
		Last Modified: Fri, 08 May 2026 16:47:07 GMT  
		Size: 14.5 MB (14501418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a228817bb9e000c4076e93b45facde5c80e1f3c4f2686a18ebf1b745c47a8f70`  
		Last Modified: Fri, 08 May 2026 16:47:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ae72b3749c6b46f048554ad43f4a70d266244b7436daa0d96264da8c869d1`  
		Last Modified: Fri, 08 May 2026 16:47:08 GMT  
		Size: 27.9 MB (27858005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552a25bb2de35164571baaa1da51bac3b66a6ccf16991c28df9fba08bce6485`  
		Last Modified: Fri, 08 May 2026 16:47:09 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff7736ffea729e535e2ae4aa283086bea85583a24f72102163c890bf9a9f7ba`  
		Last Modified: Fri, 08 May 2026 16:47:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9eb2a6c471429d6bd0f2e15b8027623136a880018e32287224e82d2049fe3`  
		Last Modified: Fri, 08 May 2026 16:47:10 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8979c53e1b6e191240e6f048135903ef7bb4bee45ee92b8f0a2661c628cd1fb7`  
		Last Modified: Fri, 08 May 2026 17:43:26 GMT  
		Size: 1.3 MB (1271928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fea201c8b81598bb80a94ad36d859f41523410e979aa6eccb7ee415e7a6fdd`  
		Last Modified: Fri, 08 May 2026 17:43:26 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41380fe93b1fa7f2bf1fe3bd4222032c2c380f2fe6cdd9317603645be7ef167`  
		Last Modified: Fri, 08 May 2026 17:43:27 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab7d57e5d7962085ce7d5919b865ba35a1c919245aea41dda35b9bc97f68a17`  
		Last Modified: Fri, 08 May 2026 17:43:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e54bfb7dc04f02b8da9e24cfb940ab47619e944dbf0a1677cd93549df7ad4c`  
		Last Modified: Fri, 08 May 2026 17:43:29 GMT  
		Size: 21.4 MB (21352171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:942d4b32bc66bd7e2bc859597216d51da99931183451d66f2f710815d30c4448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6368742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40987fa69d785d72a96f81a5177a524ecbc9b0aaaaf9e439598bd461df542e4`

```dockerfile
```

-	Layers:
	-	`sha256:a3d2e0166ddb4281ba1f555cc701dc227d25ffaa2d1afbd7f52f4a623e37f374`  
		Last Modified: Fri, 08 May 2026 17:43:27 GMT  
		Size: 6.3 MB (6335078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f23d38bae2068775a1f77e2e05dc063c6d38c41886ffa303e825f579bad1262`  
		Last Modified: Fri, 08 May 2026 17:43:26 GMT  
		Size: 33.7 KB (33664 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:32d0cd85132dfd1fa3263a4532a206beb6f46c875a04ba783e921bb723b66de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195210102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990da7d67f3805f0c1e667f9f96231c832efbde098074f44ccf802d7138db9ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:22:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:22:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:22:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:22:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:22:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:22:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:22:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:25:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:25:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:25:55 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:25:55 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:25:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:25:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:25:55 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 20:33:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:33:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:33:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:33:19 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 20:33:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 20:33:19 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 20:33:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 20:33:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acd3843ac71e2ac2133806963e05817ed4e49bf3aed3507ac247fbfde7bac89`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cdcda3e14f7ad32a2fa17dd9257b8e8c8058a32a8c240753f06b4e211cf7a`  
		Last Modified: Fri, 08 May 2026 19:26:17 GMT  
		Size: 98.2 MB (98169805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2112c17bd0d688e7aba2b8db925c9c2781c735f0251ac74933f1541710c5ba24`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2584227a45721e5472d92cce0b92dec31d3f13aa3f6a90b452610e32a28beff8`  
		Last Modified: Fri, 08 May 2026 19:26:15 GMT  
		Size: 14.5 MB (14503153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b61fbc024604f19a832b89a46885cae78c6603c63d976aeb7ed04e1e6585a55`  
		Last Modified: Fri, 08 May 2026 19:26:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d845056335c9e06680eed3d0dbfe5a267f2743b6a7dd99edb61ce0d578e1314d`  
		Last Modified: Fri, 08 May 2026 19:26:17 GMT  
		Size: 30.7 MB (30725401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ac4d39bd37db9fa0c449266f0d65fedf4bf648d538abe509b01203bc4594c`  
		Last Modified: Fri, 08 May 2026 19:26:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341674e3d0a126ff8bcbc7898c239386e1dc9b79e4f55fe13b85dcba37cb80e2`  
		Last Modified: Fri, 08 May 2026 19:26:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5c60d59f3358ed8fc8365ac95c351be69e4f578f418ff581bd9dcb97b54f74`  
		Last Modified: Fri, 08 May 2026 19:26:17 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eadcbf73b5a774c5bc8fb5108e683433420d4e1264b9977a9e9b67566e4c9f`  
		Last Modified: Fri, 08 May 2026 20:33:44 GMT  
		Size: 1.5 MB (1539485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d211ac111ef9765886972667e638baf4d5116c75ab7f48a058880f85adb8c`  
		Last Modified: Fri, 08 May 2026 20:33:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40812932a903577f2ce205c8b8e2ac06d192922c03efd1e1f4099fac80bb40c4`  
		Last Modified: Fri, 08 May 2026 20:33:44 GMT  
		Size: 790.8 KB (790769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8410451f1c1377f2e8842122c5d399d16470ddd9fcdec6440991c0843df8111c`  
		Last Modified: Fri, 08 May 2026 20:33:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb51476d8aa4998136fadee0930546e5b1d3a9b4dbe9bba9d6ae4da7d361324`  
		Last Modified: Fri, 08 May 2026 20:33:45 GMT  
		Size: 21.4 MB (21351949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:60c7d244b38e4d85f1eb14640cc2727cd1030c5055e663b4804ace1907ed4194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6583883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d6cfe93ba1cec319ee11bc941782a3cf36e1db1787b96295554402a3d52f76`

```dockerfile
```

-	Layers:
	-	`sha256:3d033be7f9013716fd600e78530930f6fcde0f766f732612016d9f4aa9f41854`  
		Last Modified: Fri, 08 May 2026 20:33:44 GMT  
		Size: 6.6 MB (6550187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121089b1cb3d2fdd3c23a9b33fcd440f8798045f1286016d36b89ab61a06a362`  
		Last Modified: Fri, 08 May 2026 20:33:43 GMT  
		Size: 33.7 KB (33696 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:5483e5e9a3d16725e00cf95f5ada81f0a743f026c1acb31c97b7479007fcf9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200838191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f399ff77b57e045669c181ea7e35e1e6fb48eab21b92e4471e342eed9aaf11`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:44:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:45:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:08 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:45:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:48:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:48:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:48:10 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:48:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:48:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:48:10 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:48:10 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:44:05 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:44:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:44:06 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:44:06 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:44:06 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:44:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:44:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57cd806e00f4f7571c4239f32642bddf22e2d7ea8557e95b59f994267e2c1b3`  
		Last Modified: Fri, 08 May 2026 16:48:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b5c4648efd668974e0c5e79a56de0d7a45fe92e0080d4bfa75907ecdcbf74e`  
		Last Modified: Fri, 08 May 2026 16:48:34 GMT  
		Size: 101.5 MB (101530236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae64f32f2d54c1a64fdf2ef9187d6ee29108490dce084c02c19cc577d381602`  
		Last Modified: Fri, 08 May 2026 16:48:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74075b9d4aca53f6ccf832410719ca38b67df402e77ea4791306b6591343a57`  
		Last Modified: Fri, 08 May 2026 16:48:31 GMT  
		Size: 14.5 MB (14502534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33bf3a80eac6985666435ebd907f977a88ea837a6d13bb80bd20f444737fc6d`  
		Last Modified: Fri, 08 May 2026 16:48:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f70c81311ea234539d5fdb958472ccf3575d313c1eb8f8eda79cadb8c928a4`  
		Last Modified: Fri, 08 May 2026 16:48:33 GMT  
		Size: 31.8 MB (31803428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2a6d88916b1317798be082fff5aee82cf6a15fab8efe5fbf6c5bc1929f098f`  
		Last Modified: Fri, 08 May 2026 16:48:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0179f3c8b60d78fc388ab3c590f3e49b2eb395f05662dd1300613c47aa2b43`  
		Last Modified: Fri, 08 May 2026 16:48:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ff6dc851c1476f5b226c9698de02b9b5d15b3070ceec1c2ccdca6bcf68114`  
		Last Modified: Fri, 08 May 2026 16:48:34 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de26bb500fb548a005321a3c422a510ca921b598d37464b65e09420fec72413`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 1.6 MB (1624472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86a46ccad5c4f17652316c602162516f37a5bebd50c65ad7512c43631ab8841`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fcfba87c8824b774723a4e94e1bb1aa7134e53af18867a00abb6cd519e6ff6`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104247b6c37737e3bbe9f49bac074aa035d8fcd1bc4323d530eb885f4ae1d49`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9a9a847415b874345a6c636218b08f49ded77c0df760b1de854e9d9aa22880`  
		Last Modified: Fri, 08 May 2026 17:44:31 GMT  
		Size: 21.4 MB (21351698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ad3eb587bd1feee4e4f48b7f9d97bf204ca6784c6e43eacafaaa66860cd60c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46327172b666bd8a2fb79a62f8de9f249d6a466c3b6a0b3b6814663609c5e76a`

```dockerfile
```

-	Layers:
	-	`sha256:cc097a7eaff16efd020140f7bcb55f8a97773c091a5186b8e273112f699c1b92`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 6.5 MB (6501570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854a2949c18f0e69cb6b8e8249140e9e8e3a08738ef13a570b9800c3b9eecbfc`  
		Last Modified: Fri, 08 May 2026 17:44:29 GMT  
		Size: 33.5 KB (33499 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:c4f317378335cae83b0edfffab6fdef97ad1406426c7877458b706a3173e728c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205482923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e0f81e54e9f40d69624b4dda1a54c790498ccea42100b822e0f63149e3f0b1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:06:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 02:07:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 02:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:07:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 02:07:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 02:07:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 02:07:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 02:13:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:13:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:18:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:18:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:18:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:18:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:18:06 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:18:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 02:18:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 02:18:07 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 02:18:07 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 09:43:39 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:43:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 09:43:40 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 09:43:40 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 09:43:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 09:43:40 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 09:43:53 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 09:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26f9cb740e187cb4772a93e40939279f04db15bf332e83c5cdd82d6ce0cb373`  
		Last Modified: Wed, 22 Apr 2026 02:12:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4da74e371512d746b2064ab8d31082a214f396711c5c5b0a83fbbeda17bc3c9`  
		Last Modified: Wed, 22 Apr 2026 02:12:46 GMT  
		Size: 103.3 MB (103331324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17bb927e267eaeefb0c6a9975a32dd0392b377723db62da1e6f3dd18551d32`  
		Last Modified: Wed, 22 Apr 2026 02:12:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b435a8489c89b971dd337f452516a8b0c88d34f76ca3d456b1d756b59313c610`  
		Last Modified: Wed, 22 Apr 2026 02:18:35 GMT  
		Size: 14.5 MB (14464894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaf6ae27854a8062947793d590aac16346890a4a532778a764cc7164b19abb7`  
		Last Modified: Wed, 22 Apr 2026 02:18:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cd3745545681c69f46e888e72e872b70529c621263f193e05eac48fed11a7e`  
		Last Modified: Wed, 22 Apr 2026 02:18:35 GMT  
		Size: 31.7 MB (31700939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2b42c1f80cfa8f47f0e9f30e7b659a83b822c375b2ef74fee1268cb2bc7071`  
		Last Modified: Wed, 22 Apr 2026 02:18:34 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5623ddbcc3df30a7ec3a491f0061606692eba2042f27d895a4b84e1ffb83d4b1`  
		Last Modified: Wed, 22 Apr 2026 02:18:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8866b62e5b58a872c014b0b75747a000ff87db968b147574b7cc67bb5956da73`  
		Last Modified: Wed, 22 Apr 2026 02:18:36 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16085ad055e7a425bc72fdea4640bd52add852f14531e6a5ddb5931a24d9f02f`  
		Last Modified: Wed, 22 Apr 2026 09:44:32 GMT  
		Size: 1.8 MB (1752514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a107b0309d5d4a273da12a4b2e0850aea92ee22a1b828ed02728074c151fc540`  
		Last Modified: Wed, 22 Apr 2026 09:44:32 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e8598bc86dfbd820e1fa0c29ba76461b193ecfe4ab2ce82e933670bc28626`  
		Last Modified: Wed, 22 Apr 2026 09:44:32 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a585fed34657340badc45bfabc2c68ac04f60783ca833be57cecff2d5698b02`  
		Last Modified: Wed, 22 Apr 2026 09:44:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d75c9f8d6b4fec9ac88d658b6c2253ffa2636c4e29d7999d3da3c01e2aeb1e`  
		Last Modified: Wed, 22 Apr 2026 09:44:33 GMT  
		Size: 21.4 MB (21350723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ea92ed6dabdf5a2810f7561604ca3e4f289322f870e69fb5619a757d0d974bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6532104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4a17e7e7f87da90e92bb5c42948f88758b46184894bbac15f956f5393c2265`

```dockerfile
```

-	Layers:
	-	`sha256:aa4fb59721b93e5270a2286d8b986fcbaf68a13ec4367bbd8b46601ebd9f719f`  
		Last Modified: Wed, 22 Apr 2026 09:44:32 GMT  
		Size: 6.5 MB (6498504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e430f00aa5533f17e484b315bce8a06a75e9cecbd40898a0fda57383d4284ce`  
		Last Modified: Wed, 22 Apr 2026 09:44:31 GMT  
		Size: 33.6 KB (33600 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:61e4503851b622ce6dc349b637ca170b3eca0d3f19b20d8746d0efab0d669374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175468414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee6cd41963b1f724d46cb451e3396dab7c7ce82d60aecf16dc3818129a0f925`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 23:25:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 05 May 2026 23:27:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 05 May 2026 23:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:27:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:27:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:27:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:27:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:45:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:50:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:50:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:50:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:50:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:50:33 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:50:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:50:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:50:33 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:50:33 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:41:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:41:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:41:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:41:47 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:41:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:41:47 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:41:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:41:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89426b8fd56cf7223dcb6f2d483a28c283ea2b89b935bab9c163d3ed348cfb24`  
		Last Modified: Tue, 05 May 2026 23:40:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961f6f8d278a8cf07820de911bea1c70cd3c2595a84e262b33067b67264439f5`  
		Last Modified: Tue, 05 May 2026 23:40:26 GMT  
		Size: 80.8 MB (80830056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959462e04a24bdbdff8d971b3748ac4a219124937bd4265cff676d017337e45`  
		Last Modified: Tue, 05 May 2026 23:40:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212deb4e82c24032fdbce0273987c23c0451279dc76c9af8e98c343eb0afb687`  
		Last Modified: Fri, 08 May 2026 16:50:57 GMT  
		Size: 14.5 MB (14502399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c784f594da3daf63961e48ac9a058fd97dbffae71a0f160c823240feefed888a`  
		Last Modified: Fri, 08 May 2026 16:50:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3472c0fd35d368e5a4d0fd7b335fdc489d4fc798b0a6caa7178cde1572f09c18`  
		Last Modified: Fri, 08 May 2026 16:50:57 GMT  
		Size: 29.6 MB (29625299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da1caed543680bbf26039ed80bdc9e28d37163a16a64e96ff73e87614d1c8da`  
		Last Modified: Fri, 08 May 2026 16:50:56 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58461980b2b63e8126c7afe0ae7c802fd526313ea7469b9b3fa410df66846d8`  
		Last Modified: Fri, 08 May 2026 16:50:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c1e027c23ff7fca2386f564020d53dce1e1b69c14cc6b9d86ff008b66dcecf`  
		Last Modified: Fri, 08 May 2026 16:50:57 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6e09549ace650afc2736ff4fcd31d8c8fac1cea5ce8213c8cf42a0598e9278`  
		Last Modified: Fri, 08 May 2026 17:42:26 GMT  
		Size: 1.5 MB (1462525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b22150db68a13eda921eb7baed406ab88005d4ca11b391414b9d10e89ba570`  
		Last Modified: Fri, 08 May 2026 17:42:25 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245df5ec7a7096cd48cad73c5b4d2cc90372ce65d5646111acbfefc03a2fe876`  
		Last Modified: Fri, 08 May 2026 17:42:26 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c987a2707b1d2ff87e8489696c4437aae7334732abd3faffd1d894f57a916e`  
		Last Modified: Fri, 08 May 2026 17:42:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670ecb1a8929d2e0c4ef39b55da686ed9cf1db36bd8d6acb6e363a80a18a8a59`  
		Last Modified: Fri, 08 May 2026 17:42:26 GMT  
		Size: 21.4 MB (21352454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:97534bf8ebc8ab142a3b2c9ab9725fb0f0517a28fc83c1420ab936774909def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6392544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f3d2e74069d32c4a5b9b6d5d5a2f6a53c89a7c7d9d785bb8b626a646692df9`

```dockerfile
```

-	Layers:
	-	`sha256:78e5f7948194c540a7bd6db9165dcaced6378b1331c939ff196c45be93aa6664`  
		Last Modified: Fri, 08 May 2026 17:42:26 GMT  
		Size: 6.4 MB (6359008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b61310499316ad671751233e7ca922eeb48f4e73c06be10a2e9bd6267fbc854`  
		Last Modified: Fri, 08 May 2026 17:42:26 GMT  
		Size: 33.5 KB (33536 bytes)  
		MIME: application/vnd.in-toto+json
