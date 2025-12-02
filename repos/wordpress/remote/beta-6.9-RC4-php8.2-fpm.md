## `wordpress:beta-6.9-RC4-php8.2-fpm`

```console
$ docker pull wordpress@sha256:7fceccbc53d8d521b685a5170f03fcb6732862ff9084fb2754d460fbb4938941
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

### `wordpress:beta-6.9-RC4-php8.2-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:26b2b8ecfd63a2b571a55a2bbd066ca443737ce5b6fb7204f87e9a634c403745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258929253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e582ae86a81dca0e7be694bf20a105d0e3efceacf9b021a2eb6ba8691f58aa9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:42:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 04:42:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 04:42:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 04:42:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 04:42:28 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 04:51:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:51:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:53:57 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:53:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 04:53:57 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 04:53:57 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:17:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:18 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:18 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:18 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee0a9a1bffe3e542e5054fe913b00319a1b32d32f2e6c2a5b402de2009fc8d`  
		Last Modified: Tue, 18 Nov 2025 04:45:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08c785176ac8b597dd7e8219a411dd00a418b71aab6d8c6bba5b3d0918357a`  
		Last Modified: Tue, 18 Nov 2025 04:45:55 GMT  
		Size: 117.8 MB (117837527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b798d58ba3ac849459814ba0526d8c0f283bf04ec83982b381aed0a04e2f84`  
		Last Modified: Tue, 18 Nov 2025 04:45:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4926a813485af1b9f278ba97e3d4e131cc4d779d189fb638a8277ad777a701eb`  
		Last Modified: Tue, 18 Nov 2025 04:54:15 GMT  
		Size: 12.3 MB (12309832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca347cd65dfb0146a176e327c0da1b2848768fe23717942fe54db19e1bd67931`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97492cc1170fc67b38439bddf091292d6f1f6f074f43788afd6a5d49edf3359`  
		Last Modified: Tue, 18 Nov 2025 04:54:15 GMT  
		Size: 11.6 MB (11643417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a246504dd7395de19830d5cc11b712a5c4bc0565c298238bc031ab6b9abfbcb0`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197e0d68e6fcbde5a2bb3d01a5c9d978312ac31ea5ff98afb7906b4b9aecd90`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe784d35c9de75603d3827fe5289a66dca6dfb0587e7bc9402cf6f6459608e9`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616ff5172131ab585e81f93fadc5fc9d978cd58b2b32452fa2abca3ff5cd3d30`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0938e9da6855af4ef74028fa0c066ec8985a2904927c9b758dc63db6a616415`  
		Last Modified: Tue, 02 Dec 2025 01:17:45 GMT  
		Size: 26.4 MB (26414918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071060f154ab3abf86774b54cc842a50ee03565585743d6fa765c31f84aeda74`  
		Last Modified: Tue, 02 Dec 2025 01:17:45 GMT  
		Size: 33.9 MB (33904235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932f43004e47e5d83aa75bbd526dadc71972cdf7c442de18bcd8aa9049e3b8ee`  
		Last Modified: Tue, 02 Dec 2025 01:17:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d0e84718642f4421b5155337cf69e06b22bc58edd8e7e0592147eee46eb09`  
		Last Modified: Tue, 02 Dec 2025 01:17:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4a194f36a5820fda1b4db8078a0f7ebc08aaefb9db878f17c2e64e5735f1b0`  
		Last Modified: Tue, 02 Dec 2025 01:17:46 GMT  
		Size: 27.0 MB (27024623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1167c351255b4a4b7b9795891c25eff156e4898e627a0aa5802b5c8adbb5042`  
		Last Modified: Tue, 02 Dec 2025 01:17:42 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd490ce3234329e4396f5c255449dc17cd18dde7d6f87c7f950a72c0924d7c43`  
		Last Modified: Tue, 02 Dec 2025 01:17:43 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0c9124c6f9b9f58387685abdca73100fcfaa7bb4b3bfda90d84492a333ff6a`  
		Last Modified: Tue, 02 Dec 2025 01:17:42 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:49a111424ed8320251a77a2d16e74b4d41e1523b84fc2026044cb23bda57937f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8200395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af1cbd86cee0576ff000eaaab6975560d3a75a61f1b852701284c14eaefee3`

```dockerfile
```

-	Layers:
	-	`sha256:c368e97f61a986f3df339fdcfa944cb26388830916b7378e7a32b17909d6517c`  
		Last Modified: Tue, 02 Dec 2025 02:26:50 GMT  
		Size: 8.1 MB (8148349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17eb5b81455a915128d905175215e85180f4259c4ff197a3edd8dc87c546c4a4`  
		Last Modified: Tue, 02 Dec 2025 02:26:55 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:863b22984d89069787d1b30f9feadf58e6705011ebd32872a47c2160b15a2715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228490921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518bc2ba14f760ca514b24c46ff026c0fea436cfb2b27bb01e1a017134b7b346`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:28:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:28:52 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:28:52 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 02:52:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:52:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:55:42 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:55:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:55:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:55:42 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:55:42 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:16:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:16:26 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:16:26 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:16:28 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:16:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1f7c1b6a8da78609720371df2b9efde52729fbf57efcbc23dc292ccf520291`  
		Last Modified: Tue, 18 Nov 2025 02:32:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb94523f6af25d0f2a3576eecc1b8009f2551fb617576dc5e3714427f17bad6`  
		Last Modified: Tue, 18 Nov 2025 02:32:43 GMT  
		Size: 94.9 MB (94873798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8169648b5d195f9eb10c1b274b485d68ca7b62bc52f8187e44922f0ebbad3d01`  
		Last Modified: Tue, 18 Nov 2025 02:32:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb00fef4dad79eb201e9fecf3c0de3c34da2bde583215db5b06f1863e93cc47`  
		Last Modified: Tue, 18 Nov 2025 02:56:01 GMT  
		Size: 12.3 MB (12307435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3052da90a478342ccba8be27330a133b53abd8240bf329197516956912623819`  
		Last Modified: Tue, 18 Nov 2025 02:56:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae6e82054dd8f144075233d33743e14b0e3740910d514f8fdf05ea198c5118f`  
		Last Modified: Tue, 18 Nov 2025 02:56:01 GMT  
		Size: 10.5 MB (10460237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32942fe0a7c8b4c2507a1e1d7976753894a990f5c53573a4e50d7bf19c212a77`  
		Last Modified: Tue, 18 Nov 2025 02:56:00 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6802012c2a2b7c939b30bee7ff9cdafd6aeae13d006cf17fc73d5797106010`  
		Last Modified: Tue, 18 Nov 2025 02:56:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20b045e650743d1fcd432904eb587dcba212f851aadfa756df30dc6af68a52`  
		Last Modified: Tue, 18 Nov 2025 02:56:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6882ae46d595a884c6f8d87e947f9ba1e14e4fc7df0b4a28d16e1a6e62b0b798`  
		Last Modified: Tue, 18 Nov 2025 02:56:00 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a96f62b110b2e7e573440c17dc5987f678caf439ffdc7f120d2ba0d063382d6`  
		Last Modified: Tue, 02 Dec 2025 01:17:09 GMT  
		Size: 25.8 MB (25836291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efac6eabcd5006925cba509ea1726ddc7dcd4beedd68b3ba49bd7bb062dd385`  
		Last Modified: Tue, 02 Dec 2025 01:17:11 GMT  
		Size: 30.0 MB (30026171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca853ccece0030e15e4fde4a43178de729a4de4c8bd078abb2bbdd70f491e1af`  
		Last Modified: Tue, 02 Dec 2025 01:17:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c609c7fe4ae15fca9ced00f1898b39f47fafea007d8eca4cf7b3daa9beedde`  
		Last Modified: Tue, 02 Dec 2025 01:17:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36aba0a29c98789edd85c964318ec1df38f6e2b2600276627357be6f0825157`  
		Last Modified: Tue, 02 Dec 2025 01:17:10 GMT  
		Size: 27.0 MB (27024621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f4c43c36f492c6841157ac86129c79984c6815d3f0c85ee409f6da13ba8b8a`  
		Last Modified: Tue, 02 Dec 2025 01:17:07 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6143dc522a8fa0af60c92f3a7008fac8b4f87b43e2973d252b58a5040b1ccbc7`  
		Last Modified: Tue, 02 Dec 2025 01:17:07 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c94e1e695e7661ffd526ea08be72230695cd105fff85a96cc5020dcf1b5e05d`  
		Last Modified: Tue, 02 Dec 2025 01:17:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:031cc76d59082cf5578b37a5784c81205a4d485decd0038860b048a8c17ff39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7999518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1649f952376ba8d795978cdbc1302a34582f6c0572ca6246474a3d5ef8b8fda`

```dockerfile
```

-	Layers:
	-	`sha256:042121b1cc8b5f93a12f6fba3f8d647551c653f3f665b1103d435f4b5baca5cf`  
		Last Modified: Tue, 02 Dec 2025 02:27:02 GMT  
		Size: 7.9 MB (7947336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e28585977c2207fe18b9c106b17dbec7a05934945f280a71755654928352b35`  
		Last Modified: Tue, 02 Dec 2025 02:27:03 GMT  
		Size: 52.2 KB (52182 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:820a9f0596ab17b19e044735e2f9b483d46413f54b824edd2f595e1cac789855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214995020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e1970914fc78d476010c645d6f249f5db64d9f1b59bcae4fe0e4c4660a4c7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:40:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 03:01:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 03:01:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:03:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:03:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:03:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:03:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:03:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:03:44 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:03:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 03:03:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 03:03:44 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 03:03:44 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:20:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:20:43 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:20:43 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:20:45 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:20:45 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:20:45 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:20:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:20:45 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:20:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:20:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e15b2702538d58ad41d73933a9ca7ed75636e7a9193fcfd3938af3e225614`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc9c49daa937d4630adbfaea0671b63469bb895e99d2e511e0872b530c2f60`  
		Last Modified: Tue, 18 Nov 2025 02:44:15 GMT  
		Size: 86.2 MB (86246052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04dbb2611276383b057bfc6e2807539484105c24203e1c4d0a1f897e60d45d1`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8504ce6a22f240870daa67c8ba5b4b61e12860562dff057f6040492460c56d79`  
		Last Modified: Tue, 18 Nov 2025 03:04:04 GMT  
		Size: 12.3 MB (12314999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea72520a8f4c8c309c9779ec5e62e04ff433ba91aec63f0f63b17c7ef35fa23e`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec1b572df0f6d7b7298daa63845fae7f4e6081f7da192c9f5ac2e2143a0c54e`  
		Last Modified: Tue, 18 Nov 2025 03:04:06 GMT  
		Size: 9.9 MB (9853440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9f21e9a82ac9baa3f9263ffaf9ba42150ec4573b77458b78cde19fa59694a5`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36223091eb2c85ce2c93b0ca23e6dff2adfa789fa433168e5885b67ae0ccf1cc`  
		Last Modified: Tue, 18 Nov 2025 03:04:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41e388834bd23d133d1aa948878bf387b42868b537a73a1947f39f2456cc32`  
		Last Modified: Tue, 18 Nov 2025 03:04:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab9e22fe7669f17dcfff305bea8077d5ec58cf419d6ccca4b3e742388d884d2`  
		Last Modified: Tue, 18 Nov 2025 03:04:02 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e01194184330045e737632400e76fe73409858953359ab66d8ef5b4ea491a`  
		Last Modified: Tue, 02 Dec 2025 01:21:30 GMT  
		Size: 25.2 MB (25159244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b164d16cf0132943c63cdbabfd3dbfacf3137a8646514422c9a8939cc81a673`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 28.2 MB (28168473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84461da216f5da77eee489dc0a0165123e63e07886a416bf73452b644d4bab7c`  
		Last Modified: Tue, 02 Dec 2025 01:21:26 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05801354399b945c94b41ee20e835d3df564494ca37b0f53ef869f458a1b6b7a`  
		Last Modified: Tue, 02 Dec 2025 01:21:00 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3446a195455f616170d8773278de5fe936b300d5a976bc0a37b6bb2e986e41`  
		Last Modified: Tue, 02 Dec 2025 01:21:01 GMT  
		Size: 27.0 MB (27024633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e1bc081708c6d52a6f9f9aa847e3b8c377358a5c5ec05370a1a686a340f6cd`  
		Last Modified: Tue, 02 Dec 2025 01:21:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292727a309393de63535a0a0d8bb4854d8e5d0753d90b9c621cec3c1fcac79e3`  
		Last Modified: Tue, 02 Dec 2025 01:21:02 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f88d78f7d55f66ae2952ac28a258ba331a113b421423535f1feb5d341a5cded`  
		Last Modified: Tue, 02 Dec 2025 01:21:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:d260b6c8fd1b9a74297dab5383f105d8e61c771a8f444a994ed5ad718df9401f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8004308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17cbd06bc87e2e794ccd0dda683d97d40226d9b462198fa2d7498c3c4bdbaf9`

```dockerfile
```

-	Layers:
	-	`sha256:f9f886d777a6b2de97a2eea33c9bc6f4a1454721590c91f8ce25f9bdea70067e`  
		Last Modified: Tue, 02 Dec 2025 02:27:11 GMT  
		Size: 8.0 MB (7952136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6252c70bebdbfb1fdad71869d75b2e3a5dbc5c62a7a528f0f1f1bcd3eccb4b13`  
		Last Modified: Tue, 02 Dec 2025 02:27:12 GMT  
		Size: 52.2 KB (52172 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:e4ffc4d7a9daa9ce971a8fb5f4a744daae3d47c253944b858aa9a8c34d2c5c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257324864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e5d0fcc25707aa0e0ecab77098aedca0aa8b458201eb6e0a784b4a1a8f0979`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:18:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:18:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:18:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:18:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:18:21 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 02:34:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:34:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:36:53 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:36:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:36:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:36:53 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:36:53 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:08:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:08:34 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:08:34 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:11:14 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:11:14 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:11:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:11:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b7a877dc5becdaf11601a69f709a667b06b5d02891f017d80b130de42e76b3`  
		Last Modified: Tue, 18 Nov 2025 02:22:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349ae47adc1c35ad626dfcc265e1c083980b679fd0ac4ce2af4d3e7c23e17044`  
		Last Modified: Tue, 18 Nov 2025 02:22:30 GMT  
		Size: 116.1 MB (116138576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af17f59be1b3a400865c3dc929a79c2abf6f7deeb740de0542712dbef78d7`  
		Last Modified: Tue, 18 Nov 2025 02:22:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af178c25e8178766668f251963dc0a4cae6bf77095bfd969edb26894e270ee17`  
		Last Modified: Tue, 18 Nov 2025 02:37:12 GMT  
		Size: 12.3 MB (12308787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fbd5be04a3bba2b346f074bc6c3dcc91a2425ff2ff4da3f9e1595ddadee3`  
		Last Modified: Tue, 18 Nov 2025 02:37:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c7bd4833ed0f9e513f7fac6b37b2c8e030c404d72970c4d0d2d155b26c665`  
		Last Modified: Tue, 18 Nov 2025 02:37:12 GMT  
		Size: 11.9 MB (11869836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803e676b95cc8aff83390015af96cf32c9a99e01282b0450abecd149cc7c312`  
		Last Modified: Tue, 18 Nov 2025 02:37:11 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff35d5aab709e437d45e67880aed97cfe1b3bf921a9a974520d89abeb1dfb71`  
		Last Modified: Tue, 18 Nov 2025 02:37:11 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec317716ce9a2349255d1eb02bcf21f647ba5c99507a4068dec3b9871ddb38d`  
		Last Modified: Tue, 18 Nov 2025 02:37:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3e21dad832c22a3885b49a51d3690371e957eefb454feae9dd16d71ada5844`  
		Last Modified: Tue, 18 Nov 2025 02:37:11 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ad6ac8980e39796d920e91585ce1d27fb933c15f793f537309687416021d1`  
		Last Modified: Tue, 02 Dec 2025 01:09:15 GMT  
		Size: 26.9 MB (26871152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e7f4a0e2ecf986e63cf333fe8eff01f61f2c990ea4b96d9d89d581c5dc4860`  
		Last Modified: Tue, 02 Dec 2025 01:09:15 GMT  
		Size: 31.8 MB (31800587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068e6b9ab6ca87d64c0d0faff68a1b341ecd9e767ead2f6c592f79c69cbd2c41`  
		Last Modified: Tue, 02 Dec 2025 01:09:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546103b08dbe27a90d4329709b924ae34f8c4374dfa8cd0eac69ed5109d1dff0`  
		Last Modified: Tue, 02 Dec 2025 01:09:13 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7330bf4fe7807aaa2216fd1704be5cb90a39441ab05e11dfbdd937134cb373de`  
		Last Modified: Tue, 02 Dec 2025 01:11:52 GMT  
		Size: 27.0 MB (27024637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f81768a87624e1330d94127ca25b6302316431b8f8fabf383a32e140ab08df`  
		Last Modified: Tue, 02 Dec 2025 01:11:50 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8feed2038127c39789ede018d64b59b792c8d952fae70fa0963ea52d735ee27`  
		Last Modified: Tue, 02 Dec 2025 01:11:50 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f5d28969a89170399ca7fc67116a515c95f37491493b200ba70ee4acd25458`  
		Last Modified: Tue, 02 Dec 2025 01:11:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:843742aea1138be270e83833e37e7f86fb0dc7e84b8392f437214dcb43c9eae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8c75af420b4b4475dbe38612bac2d5effd668042e6b996ba5e2a6674c09aa`

```dockerfile
```

-	Layers:
	-	`sha256:07691d0487b8eb5d4254560cf5cca190f6012c219d97ce9a6e02345ed564e094`  
		Last Modified: Tue, 02 Dec 2025 02:27:25 GMT  
		Size: 8.1 MB (8121409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723fff888fa6d879ca6024e6937fa8b0f8b7bcb22b0a6e7ead76fedffeab24c9`  
		Last Modified: Tue, 02 Dec 2025 02:27:26 GMT  
		Size: 52.0 KB (52004 bytes)  
		MIME: application/vnd.in-toto+json
