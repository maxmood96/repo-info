## `wordpress:beta-6.9-RC4-php8.1-fpm`

```console
$ docker pull wordpress@sha256:a5ac6f9d90799be13f9b7f0fe36389a896a4ba7ea635be9017d504dc30f8ace8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.9-RC4-php8.1-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:6675d674f7d10b211d7a32368c65ae2341d21ae4b3726e557c1492558ba60bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258355231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701b4f6b4369ab6f3d97dd504a547c54bd1822c2e0907048977c252e43846c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:25:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 04:25:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 04:25:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 04:25:37 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 04:25:37 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 04:55:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:55:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:57:59 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:57:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 04:57:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 04:57:59 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 04:57:59 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:17:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:20 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:20 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:20 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b41e94c0a0ef00ab5d780fcbc953290d5dc3b052be8bf154e66cb0320ec00`  
		Last Modified: Tue, 18 Nov 2025 04:28:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ab2ef5a3e4e83e282e275df009e53ba3016eaf676ddc2b52906f31f9b5c1d5`  
		Last Modified: Tue, 18 Nov 2025 04:29:05 GMT  
		Size: 117.8 MB (117837804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d232b3d82a30b585dd00199ea3ff88dbc0ee0df9d26a766fa13749ee9e856d`  
		Last Modified: Tue, 18 Nov 2025 04:28:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9607cfa265102eb5725acd551ffb146fbe5e3a51be845a05217969a9cfb6882b`  
		Last Modified: Tue, 18 Nov 2025 04:58:20 GMT  
		Size: 12.0 MB (12046489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb91df444914d15dada17d70c449617dc547840265ad16974a74251191e7ae4`  
		Last Modified: Tue, 18 Nov 2025 04:58:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebe495b161c04c440d58122179c7c2740a34923173b17f5cd8a4a211a40ae82`  
		Last Modified: Tue, 18 Nov 2025 04:58:19 GMT  
		Size: 11.4 MB (11375553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f56501b9f4c3184a2a97011f371138266e4eb29b510ceae6e45b21db56a01`  
		Last Modified: Tue, 18 Nov 2025 04:58:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bde5b926875fdca8a16996dedb473248ffa50e1b2d4f539ee910861b69b099`  
		Last Modified: Tue, 18 Nov 2025 04:58:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f76acd08cf559814a1d3a4abb9eeb72aef41bb94a2b12a8cbb7292824cc44c`  
		Last Modified: Tue, 18 Nov 2025 04:58:18 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4684a9728faa17c17be1c9c22159683c9a1185977184242369c5fb22b972fe`  
		Last Modified: Tue, 18 Nov 2025 04:58:18 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c5a6bb3a8565238bd1fb10b41bfbe4aab2cc5d607fe673b32bee563e3bd866`  
		Last Modified: Tue, 02 Dec 2025 01:17:51 GMT  
		Size: 26.4 MB (26415018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dbe6295f7e1cbe58da17198f4704666b39e6f56193663026a36fe1fcc6f04`  
		Last Modified: Tue, 02 Dec 2025 01:17:53 GMT  
		Size: 33.9 MB (33861354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46a15b4166c97a955b1963d7351b23e66555774ffa2fafcdff4bfdc5c649c24`  
		Last Modified: Tue, 02 Dec 2025 01:17:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c9e0b0bcd61687ff392b177657a1c331d4cc59d0b270a5446c71087302310`  
		Last Modified: Tue, 02 Dec 2025 01:17:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c0373205a29323c904500a49c33a3918245962342e438a1c7c8081ad4cc725`  
		Last Modified: Tue, 02 Dec 2025 01:17:51 GMT  
		Size: 27.0 MB (27024639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c150a7bf23e9fca9a2b4ec0e95e7aa3b09b03045ce19d15238641b4d51ad83c`  
		Last Modified: Tue, 02 Dec 2025 01:17:49 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aaeabe90e703d8036ed7e6bb0541b936e7c0f73f01d8e0e8fa637ba562b958`  
		Last Modified: Tue, 02 Dec 2025 01:17:49 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b139b4382edd134ee86aa2eca1ad2b5c8f0af592c8e62c3c5647ab3911da95`  
		Last Modified: Tue, 02 Dec 2025 01:17:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:7e647b2ef10465422e80550bc3be027357391c18c11a1fb08a8a589157f2de4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8200395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ee75d131222bbd94e97415eeef7dd7d225aafe96b4e20cb12f6d36d1851a3`

```dockerfile
```

-	Layers:
	-	`sha256:be8c1cb0dcb50dd61939634cd5b85399c8a730696e8a8b67cdde718b21379da3`  
		Last Modified: Tue, 02 Dec 2025 02:25:48 GMT  
		Size: 8.1 MB (8148349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157375b41e55508776d863699d02cda032678ce4e820f50b1a3b4ccd44dac1af`  
		Last Modified: Tue, 02 Dec 2025 02:25:49 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:539d9128e676a3a6a03bc2fd2e11c8b0884a8d0d054ac7f3bd3c36ef647f94bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227874613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cce16ee03c74f689f9466cfb35ad711218a2ea43025b629aaa18744db835bfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:28:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:28:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:28:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:28:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:28:57 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 02:28:57 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 02:58:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:58:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:01:00 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:01:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 03:01:00 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 03:01:00 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 03:01:00 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:12:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:14:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:14:05 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:14:05 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:14:07 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:14:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f717fc6a32ce284df3dcfb5d183cc538f8a3b0ae7e0992758dd3d3f5bc043f75`  
		Last Modified: Tue, 18 Nov 2025 02:32:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5595e210ac5ed612507e279049c0ee2aa53e74d182e8b516741f61f6ed20263`  
		Last Modified: Tue, 18 Nov 2025 02:32:58 GMT  
		Size: 94.9 MB (94874243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b00a4f097cdc344c9784ca183aa3946503244c01daa04e64e176c0a734b057b`  
		Last Modified: Tue, 18 Nov 2025 02:32:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cc545ed5af7e2697eb342161b5234ee7e8d273e860482c584a4eea719aa0c2`  
		Last Modified: Tue, 18 Nov 2025 03:01:26 GMT  
		Size: 12.0 MB (12044043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d790daaaa24a5969883a8fd75d49747f91141242da7529aad8a420ddcad9cda`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f19c10311f919e0ddc05314cc5385062b4fd2a74921e395a4753f005523e83b`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 10.2 MB (10172859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20b7e6eaee4d881f9c7322c72906f332fb7d2769fe0a0ffc7c6a0875167b006`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304383afe0a720fe064c65830c857dedfd9bc5c7f4d8d0be8922b2b42792614d`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4073304d529ef2b9cd0593259c015c9048a2c8ec043efd8586b5a315707be0e6`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c824db7797f5a8e124e84c745cb9237379e9db3254bf54d0ebe032c625c53081`  
		Last Modified: Tue, 18 Nov 2025 03:01:24 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239d1361b3d25504d38a112988586422e2cdea394adf3356fca415484341ecab`  
		Last Modified: Tue, 02 Dec 2025 01:14:48 GMT  
		Size: 25.8 MB (25836255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f87dd134fc43dfbf1e4227051b8947d54297e45c8c6d6f04b510b1d49562c5`  
		Last Modified: Tue, 02 Dec 2025 01:14:49 GMT  
		Size: 30.0 MB (29960532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100545a2232b711577d89bc9831817fb894aa0d5ce211479e0d1f2ecb558ae4d`  
		Last Modified: Tue, 02 Dec 2025 01:14:44 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409ab21a1ad08d36f79b2a227597a4a6a06bd63e3e1d4adc63581b40e9d151f`  
		Last Modified: Tue, 02 Dec 2025 01:14:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e08322176772a11f1c8fad83ac1b8d096449a4b57560f74960c9b18e8ac70`  
		Last Modified: Tue, 02 Dec 2025 01:14:51 GMT  
		Size: 27.0 MB (27024621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deebb56a6666ee0a8a0548cbbe0cd802beb27f3a241beeb3c54f2e968515ff62`  
		Last Modified: Tue, 02 Dec 2025 01:14:45 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375d3ac9ba4520efe410911bced24e33c7888bdf0942332bd0180c3fc326313a`  
		Last Modified: Tue, 02 Dec 2025 01:14:45 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360568e29c02cdc6acc1e71856660af496964d89a4db1a4f0546a4cf15ec0c7`  
		Last Modified: Tue, 02 Dec 2025 01:14:45 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:ce5f8d84e87a5273a2c63cd8d8474e92f5c7eb8909a04aa0c6aab13ba154f67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7999518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ce093621780e89a1cc42eae1f533e5530014b9f3b0cd82badd3b1462ce2e73`

```dockerfile
```

-	Layers:
	-	`sha256:1d72f9ecb184467042807a5d253425c9dde7d0ed277d59fb0208cebbba1a6ce2`  
		Last Modified: Tue, 02 Dec 2025 02:25:55 GMT  
		Size: 7.9 MB (7947336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd60b8710ac2936f192fccd4a12a79c18b0f9c0f696485343c5ef0d452844610`  
		Last Modified: Tue, 02 Dec 2025 02:25:56 GMT  
		Size: 52.2 KB (52182 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:d290fdd741ec701d86b4ec8df5d6a33e9c70ca992ce7c5a8db7637ef6b767287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214414226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22577934b1d64c15d587bc34f8ed15062b0609bdb1a7f42ad14657a4385f4e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:25:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:25:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:25:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 02:25:55 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 03:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 03:05:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:11:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:11:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:11:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:11:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:11:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:11:51 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:11:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 03:11:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 03:11:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 03:11:51 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:18:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:19:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:19:42 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:19:43 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:19:44 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:19:44 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:19:44 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:19:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:19:44 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:19:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c1501714e4aced429b3a92adefec0532bf2f2123b542543c8bcb4a677cc7b`  
		Last Modified: Tue, 18 Nov 2025 02:29:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c7a8d7da7b029ed36f3623029bbc0a21c693704badf77059c3013ef143b39f`  
		Last Modified: Tue, 18 Nov 2025 02:29:30 GMT  
		Size: 86.2 MB (86246287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a926ccb95b3f0b45bada5b88b09ac10244b7184661ffc47d93524139b9456e`  
		Last Modified: Tue, 18 Nov 2025 02:29:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9201b27f94a278eebc16364da099c3d58238a48e211f32cc14c83d76b0334c1a`  
		Last Modified: Tue, 18 Nov 2025 03:08:40 GMT  
		Size: 12.1 MB (12051941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cce42ba2d0d6296deeeb2d8ea0c9cd96e4aaf13544fd72e3baae6bda5c53e8`  
		Last Modified: Tue, 18 Nov 2025 03:08:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b1240f326ba8cc9fc50c43ad38c7049484aeb61435f70c163231ada31a096a`  
		Last Modified: Tue, 18 Nov 2025 03:12:08 GMT  
		Size: 9.6 MB (9597653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc23cdea74208786e87f87710dae16114307e8bde02fe9a5844cf6ceb08b843`  
		Last Modified: Tue, 18 Nov 2025 03:12:07 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8ff7c9aae61a2123d7334ba65eee06d8d2706ac30c3893f09c9abc3c0b7088`  
		Last Modified: Tue, 18 Nov 2025 03:12:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195aa50176d9094592e9438410c6f56dffb2945f89b12f3d20670c9708b583c`  
		Last Modified: Tue, 18 Nov 2025 03:12:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bffa29168a8b7ef338d7efc2f20b5d839a0f71f85555cfdff916cf942a41a5c`  
		Last Modified: Tue, 18 Nov 2025 03:12:08 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca06f5ef1df9eeae19d33c1975836b62b2525d766c7360330b649bed87bd1dd4`  
		Last Modified: Tue, 02 Dec 2025 01:20:12 GMT  
		Size: 25.2 MB (25159168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10cf665fddfa9de7dd9f41a93336978fdebe7fc4a0dc5bd2d47c94b1019738e`  
		Last Modified: Tue, 02 Dec 2025 01:20:09 GMT  
		Size: 28.1 MB (28106655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e08c83f605c2d46fcf0f13316de776a04d71b1241783e9a9ea8e38b6bb7fc1`  
		Last Modified: Tue, 02 Dec 2025 01:20:07 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8a783af46e2f40743ca5501358a9c57c5a98d9408b36882ea34e9a98bccc21`  
		Last Modified: Tue, 02 Dec 2025 01:20:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617fd61794f66b00ae6543cdd3a292a82d01cb838b01959183d72daed1e2201`  
		Last Modified: Tue, 02 Dec 2025 01:20:10 GMT  
		Size: 27.0 MB (27024635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04a3cc64a446342fa5304bc9420968e0371be157fb423f7680848197fa83bf0`  
		Last Modified: Tue, 02 Dec 2025 01:20:07 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52391626aa796b5499f98b0509f238ae34de84aa00c1e61311ecb1c8d6686865`  
		Last Modified: Tue, 02 Dec 2025 01:20:07 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9ca63abeba5a5b777d1a706a54788d25e6c45b94e925e98398ecd2344e5fda`  
		Last Modified: Tue, 02 Dec 2025 01:20:07 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:1c3eb35b93c7c347ecd9cc5c62c4c155e5197ff9ff5e17fa632c2e36beb9b899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8004309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e3a6956f930ac237cd135ae3be5dd6ed4dbe6922279b645d0061ed82d2c165`

```dockerfile
```

-	Layers:
	-	`sha256:7a085057387b763d6cfff5ad67f337157f5302bc2d898f452d570740453e9995`  
		Last Modified: Tue, 02 Dec 2025 02:26:06 GMT  
		Size: 8.0 MB (7952136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af184a2b2587dc3cfa641df41909e451fd1ae5fc982f89047b03837ba14a66c7`  
		Last Modified: Tue, 02 Dec 2025 02:26:07 GMT  
		Size: 52.2 KB (52173 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:20991d1e8f0a87d5dbbe0e59e02037020957384250d6ff2c455e4e9f61bbf92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256732070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962f29e1b4fa2137cc84507ff3f5289ca7c989b7c0d44472646dace97bf6257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 02:22:34 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 02:37:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:37:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:40:01 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:40:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:40:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:40:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:40:01 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:11:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:12:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:30 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:30 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:31 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:12:31 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:12:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:12:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:12:31 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:12:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:12:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e5806b99c633d0cbe5a40bb1c3a001819e5920951ba0c45ac35621c62919c3`  
		Last Modified: Tue, 18 Nov 2025 02:26:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba2dcfde96736b8d7c95790231a3631acff4e0bb7f3fa191c0eaacd62634d9`  
		Last Modified: Tue, 18 Nov 2025 02:26:12 GMT  
		Size: 116.1 MB (116138520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bd16c4b13d38a3e7495d05aab1372abb17355bb95a285cfb22420dea45ca33`  
		Last Modified: Tue, 18 Nov 2025 02:26:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45661a3e8f248dbbbd65c63381d1c6063cd0aa98789cfce0683f92d53a9c47bd`  
		Last Modified: Tue, 18 Nov 2025 02:40:18 GMT  
		Size: 12.0 MB (12045392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc542d13f413e7c1fca277863fd0a420717215b76e773a4315760a2a93c145`  
		Last Modified: Tue, 18 Nov 2025 02:40:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38de2fcebaf45ac6a8d5dd8c4d7df02f1ceec13c9ad0960ba1c2e9cd53ca69`  
		Last Modified: Tue, 18 Nov 2025 02:40:18 GMT  
		Size: 11.6 MB (11586088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7895f47cf31f76a2d4f4872ef4f259d785867e19006a8748d17d1cea8b5cd6`  
		Last Modified: Tue, 18 Nov 2025 02:40:17 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eab1bc350be2da3d4dfd8e77e412a77eed7384b8460212a8a09c073998a7055`  
		Last Modified: Tue, 18 Nov 2025 02:40:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6871e17fa47aeec9748c76c7438bb3e497a7db013d5740f14a73b72f9d1902`  
		Last Modified: Tue, 18 Nov 2025 02:40:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3c96d44a1d51012134ff5d5a410cec800c6ee81f8398a4ec74710d33517501`  
		Last Modified: Tue, 18 Nov 2025 02:40:17 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de43c467c077f317b995a72db78f51d189f0ac6984f933cd05b3a154fa9d776`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 26.9 MB (26871205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602f5aac603a6efa9d14dceaa2e926b55ce2706b609d6e8b32c65fc16a8405d`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 31.8 MB (31755234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3b934ea55ba924bad1e7c133a823ac1e22c395990765c9d647b8309754a3e9`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad326faa8041b557d77af14d1a067858d8e271f1566454e8b8c79908f66bbec0`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab28c85c3ced7be65b48b83ad863b5ead04b369bf8ddc94e44c0a9c4da59ca`  
		Last Modified: Tue, 02 Dec 2025 01:12:49 GMT  
		Size: 27.0 MB (27024639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adac94a9f5a1dbe6e8730aa2dea38343f642f78bf84f3b0c4a739c762ac8757`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c56104a238b613a3bf4e9c324e3e933690b30f290903a8ec80ecb72be9500f4`  
		Last Modified: Tue, 02 Dec 2025 01:12:49 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18158f8ae811d70b796b537bc9a0804abbd78c984f9a6f4bf290ca412f9c3aca`  
		Last Modified: Tue, 02 Dec 2025 01:12:49 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5183e41cf5aa695c8b253d6b2d88731659a8a51792d981231c69cb192385ef50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62369469c00cb077c404db2fcd3725ad37feb5d1988e4037b9a829e6540d3d6`

```dockerfile
```

-	Layers:
	-	`sha256:373e41e5ce52351f87f85f73a8f3150efdeec1ec92b67bb76e19c4618d7286b9`  
		Last Modified: Tue, 02 Dec 2025 02:26:20 GMT  
		Size: 8.1 MB (8121409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15aceaf38135d869320eeb041a84295069a7e60c294a580923f144783de5b2a0`  
		Last Modified: Tue, 02 Dec 2025 02:26:21 GMT  
		Size: 52.0 KB (52004 bytes)  
		MIME: application/vnd.in-toto+json
