## `wordpress:6-php8.4-fpm`

```console
$ docker pull wordpress@sha256:3a3def8a8926e8e29676575bbb62a6ba8f0242c009ba907a56d5af41454a3571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `wordpress:6-php8.4-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:ebd550dbbf1e9b8287c247cf8f7399289435aada041dc076e26434edb441bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263020758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6b1093131addb578c5d4b7a141a156d0eb2952754a8d0e91b83baaf4034831`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f54bda37a0f3414da800aa09358db214706a9c41092cccd160ef85bd881cbd`  
		Last Modified: Mon, 08 Sep 2025 21:45:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82259e2cc78c6b7380ba09942db7af5255d8fa7f3da0059a61080325fa36653c`  
		Last Modified: Mon, 08 Sep 2025 21:46:05 GMT  
		Size: 117.8 MB (117835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193f06b445fe74131814fde6d3c7cb5a52eab17f173a9c9f20eb63b4a359e34`  
		Last Modified: Mon, 08 Sep 2025 21:45:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c9225ef8a0bf2d67172537a54346a22cc4809acc5b7c139444a251206c41f9`  
		Last Modified: Mon, 08 Sep 2025 21:45:56 GMT  
		Size: 13.8 MB (13783972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc13381d01714452519ac7b7ef0b253c5430eb188185a859055c002db9af2b`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a3488303e01f4139270dc55ccd4a469ca5df5a39fdaf143da0b793b7e70fe2`  
		Last Modified: Mon, 08 Sep 2025 21:45:57 GMT  
		Size: 14.3 MB (14346559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7985fc18c2eefcede4c373c00b3d0a81205f6be228fd11dae96678242aac3`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb60b8af5aad487cb92c5cc17f687d40be4b7933633cc220a4855eada8bc0eb`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfd55202c3ddb054ae394bc8f09b4104fe24014e87e3f65a11bcbfba211f5c`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9650050d44dc7ecddabda2304815d9173cdf70953803643d8d031ad6b287e6c4`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56553528c20c3982f7ea2946d8895d11f7621d195ab0d5f1f09a2ad66681059a`  
		Last Modified: Mon, 08 Sep 2025 22:31:17 GMT  
		Size: 26.4 MB (26415065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7213deb0c56a09644cbdb1d66b39b99df88a5d5b6457bfa8ded12221a9049962`  
		Last Modified: Mon, 08 Sep 2025 22:31:17 GMT  
		Size: 33.9 MB (33948978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3148cbe8d787eae33b5dd40191ff23e0425ae32f3aa039d49068f7ca925439`  
		Last Modified: Mon, 08 Sep 2025 22:31:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af31c8dd6b83305f4313bec38d4530cd12b7afec5420b49117e047f0c4adaf8`  
		Last Modified: Mon, 08 Sep 2025 22:31:16 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf8091a01c091177977a4f43f9f1e8003b681e738e84606f82084b60cd1d7be`  
		Last Modified: Mon, 08 Sep 2025 22:31:19 GMT  
		Size: 26.9 MB (26898596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf7f6dddb46b63e65e1d6ff27d0d4adaa6f0b282e6e004a5732e9e985a0a65`  
		Last Modified: Mon, 08 Sep 2025 22:31:19 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dadd3b1147438dc6eaab8ac67735d7d5b4752ebaaa47f4af707d2f011bcef55`  
		Last Modified: Mon, 08 Sep 2025 22:31:19 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45399b5328ba1a63cfd81ea97d3ac1ba183ff2619d3151fc3463b05a507a2439`  
		Last Modified: Mon, 08 Sep 2025 22:31:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:2aa36db4d9820a208ca5906274f2b23b064e19497afe8aaf5bc6f18307c00d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8199848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d4a3184d172b8880ec599fcfb3ce146dd95c2bc38722503c015f2d3dd413e`

```dockerfile
```

-	Layers:
	-	`sha256:893979380dfd5f3a634ccb9b0e043c6777107ea21594d6e44da8fb674067b3c7`  
		Last Modified: Mon, 08 Sep 2025 22:14:54 GMT  
		Size: 8.1 MB (8147856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c322ec15bd72b0e7147b8259bf3c2cccab3ed393f5e3bbe72480ed86e95f4e01`  
		Last Modified: Mon, 08 Sep 2025 22:14:55 GMT  
		Size: 52.0 KB (51992 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:87b4fcf6f6964ad26c11da9e02a9b970a19259851fb2b848e3c09764ce3390da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232335856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30508f0b165a89111ce4b2510d9b585ed8a63a281cb400322edecc887bd85539`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8956d940413107e8a587889282d89e7b056b270d4521a0fb94cd24b6b45cb9aa`  
		Last Modified: Mon, 08 Sep 2025 21:35:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54422b440865b387ae4ee5ebe83477e636240c0894f7885c2391dfc6a1d605ab`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 94.9 MB (94872271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5293bb11cae50ed59c799b4dd0ea0db2f1f717e070a56ccfd00bc4d87cee1`  
		Last Modified: Mon, 08 Sep 2025 21:35:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051baebb2b7d5391ca347707e9e0f24fd869bb7339f5ac724f9f64a200c44c1d`  
		Last Modified: Tue, 09 Sep 2025 00:02:32 GMT  
		Size: 13.8 MB (13781532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7df078c62011cb3c0ea9d195c8327c0dca4fc7c68317583730f3ac9e7304d7`  
		Last Modified: Mon, 08 Sep 2025 21:35:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575e7736797a10e20a001458febc60ff0e764668ed5f3b4662d71f4409bc5bf8`  
		Last Modified: Tue, 09 Sep 2025 00:02:34 GMT  
		Size: 12.9 MB (12918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcae26b0724a9cd1db378dfdb7b574043357c761f4c196f735fba7e40514764b`  
		Last Modified: Mon, 08 Sep 2025 21:35:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0defe3bab8285766d7f3150451759934cd22d0f2ec8dfe43e051709a235ec9`  
		Last Modified: Mon, 08 Sep 2025 21:35:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc4e6507667159f68f0976883ff1bef2ec5b989327531ec3583e1b982c36b98`  
		Last Modified: Mon, 08 Sep 2025 21:35:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed00cb49697ab71c93d11a8bc6bac217f489d10bb2f8518529a37f970cd7ea3`  
		Last Modified: Mon, 08 Sep 2025 21:35:36 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e25080e85cb1b8b1790b612c5f21697b40c275730efbfe3fee100f55aefddd`  
		Last Modified: Tue, 09 Sep 2025 02:21:57 GMT  
		Size: 25.8 MB (25835400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80adb1ce264a2fcb853829ec2fbbfa13b8af66bc397ba1449c96b5f2a2110c1f`  
		Last Modified: Tue, 09 Sep 2025 02:21:53 GMT  
		Size: 30.1 MB (30069466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98677833ba80c78109355112150a995c878da8d17416811ad7c20997b47eb10`  
		Last Modified: Tue, 09 Sep 2025 02:13:43 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de046667ab7b701c8fe082745ad73e62f1308f62076f3576237d88b6087e85b1`  
		Last Modified: Tue, 09 Sep 2025 02:13:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da49d7055656555beda1cd2a9e435779294d60ca02ec4beaa0989a8d8d93c03`  
		Last Modified: Tue, 09 Sep 2025 02:21:45 GMT  
		Size: 26.9 MB (26898580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ba4542c4818021d696e8120c99561ddb810fedb275454cda69d983f8c5f75f`  
		Last Modified: Tue, 09 Sep 2025 02:13:43 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0fcdbd20f41fc8a8b6cbfd04cf71742f60524b086b87228e054efb2de67b4`  
		Last Modified: Tue, 09 Sep 2025 02:13:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5423c4de61705c3e95754301985148b735ff168561acad8a374670f5326495ca`  
		Last Modified: Tue, 09 Sep 2025 02:13:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:e136e29016fdba81dd2063fdd8cf45afe72d72b47a4c9930a74afe9a614afe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7998971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e943698b98066b3e7ac8264ec91ebc48d82653bd4687f7d543a180aefc89a932`

```dockerfile
```

-	Layers:
	-	`sha256:ca3830c6722207ed44cee1f1577acb481e86cac2372339a2462437ec121e9c2f`  
		Last Modified: Tue, 09 Sep 2025 04:14:33 GMT  
		Size: 7.9 MB (7946843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1e482e779c2fee7d2e0b56cef74e3df28963b8797a490cd07a7618966cb1db`  
		Last Modified: Tue, 09 Sep 2025 04:14:34 GMT  
		Size: 52.1 KB (52128 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:2c686593ce44a432dc9ed60099b3704d33ebb5d9da393d4fd71fe77e537c0b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218764249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a549d1b8ea23c1f2ef8797fed6cdf9c180cc09afda64b7a960578d47125ed9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170005e8e6b2785a58cdd86d5a05d68a9cc82b4d8846ed3f5456a9814275b203`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419eb2d7b1e735d456c74a84e6968a328f9ef7ca83b0a11e4e06114013863d43`  
		Last Modified: Tue, 09 Sep 2025 00:02:48 GMT  
		Size: 86.2 MB (86244716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e76699292edcf726849ca40ef1d4e203da4e9fe6b652bdfe326e2e916c7514`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd5e36b56e434746f82d914c5fcf6ccb75ab1064ece40ebf0902c3f04c026e8`  
		Last Modified: Tue, 09 Sep 2025 00:02:49 GMT  
		Size: 13.8 MB (13781633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cfdff1a16c85f4a7634baa3e4cbfb7bb52624d5eee063d27dd64836af844d6`  
		Last Modified: Mon, 08 Sep 2025 21:43:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c686c9f7de12f4d5ca0e1df0619ee8568e909c16937e261650dd23838140017c`  
		Last Modified: Tue, 09 Sep 2025 00:02:52 GMT  
		Size: 12.2 MB (12249571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f80e4eaa7c5ec476e1144b9d562abb629a39ec3120dc560d6812ae6c7dc78`  
		Last Modified: Mon, 08 Sep 2025 21:43:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63be6006f58ba6c3e4147f460b80c2aa2efa395f6b83055e8c819b451e46e5ff`  
		Last Modified: Mon, 08 Sep 2025 21:43:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2f4961c54176b80f4bfa93d447265712ce48cbd2576ad9752f536e5f9cdf1`  
		Last Modified: Mon, 08 Sep 2025 21:43:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b65579a3664bba24091a057d88213a92245d4bb02494e41741cf9804c32f9`  
		Last Modified: Mon, 08 Sep 2025 21:43:18 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbd81cf041a8709b8d95cfd31b55d794bc20ba36d8b66224e0fe44f681e6c4`  
		Last Modified: Tue, 09 Sep 2025 03:21:33 GMT  
		Size: 25.2 MB (25159886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c810dc91966deca7fb320e979b000187df8ff44a81a2fd46490d90a24942a0fb`  
		Last Modified: Tue, 09 Sep 2025 03:21:33 GMT  
		Size: 28.2 MB (28203799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565d265293f4f6a1c46b7bcb8d33f54db1fa4b796f0739e72cdea7d7feba146e`  
		Last Modified: Tue, 09 Sep 2025 04:07:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c4e9227f6ae83609a4bed36bbfc3c21f6142d0e19fa6ea4503de4af4f9bc24`  
		Last Modified: Tue, 09 Sep 2025 04:07:07 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027937a178bf445038a2226fb7cf9845d6a6550b5b30acc52b68adcc2039a4d7`  
		Last Modified: Tue, 09 Sep 2025 03:21:34 GMT  
		Size: 26.9 MB (26898584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67181b022d8d036af8bb736baf4f58f64d8404a711a33ad67c5c703b0d341572`  
		Last Modified: Tue, 09 Sep 2025 04:07:06 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff7c6e5eef1f2e2f40a6ff3fd95b977a3e8ee4f2beaa023d8958435fd0786de`  
		Last Modified: Tue, 09 Sep 2025 04:07:06 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52afa16d1d7b56df54b1d0abbf6c4fd20892ea7664f5d8ee67e1066d29507eda`  
		Last Modified: Tue, 09 Sep 2025 04:07:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:b27f3cf93537c1174179c6d485e61489bdf5db86934727c6cca039342ca9784c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8003770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724035aeecac8636d5d751e6611757a990d13d5d1f265f5a2a833488d808b15d`

```dockerfile
```

-	Layers:
	-	`sha256:4fde22d56ec4f56be6b8c408564548f501cbd43eb0f16b3ba31f8747402c35c2`  
		Last Modified: Tue, 09 Sep 2025 07:14:01 GMT  
		Size: 8.0 MB (7951643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ec49b31ba8cee0ad93a1f6e8944e186811c757019fe6edf2e93e06e14675d40`  
		Last Modified: Tue, 09 Sep 2025 07:14:02 GMT  
		Size: 52.1 KB (52127 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:818eea11acef543a7090443ffee08aac6fbd2e06bf866df7d17f916eb40166fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253128669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd6d94c52f6f398e2e3e3f3328424caa593d814b83ead72fd6af30302d2f6bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ece5e8db45df529c695354fb69a31fa35d96c6acc213193b3b8b0d91268c44d`  
		Last Modified: Mon, 08 Sep 2025 22:04:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5378f2f406c9f274e4864d2bf451a2bac770f09b6aee2189f9c71f82fca4c0c`  
		Last Modified: Mon, 08 Sep 2025 22:21:50 GMT  
		Size: 110.2 MB (110161802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485dc7ef4bb46555035f16886a78f2132c0c38a70d1e435ca4d7f3bba5e00c`  
		Last Modified: Mon, 08 Sep 2025 22:04:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326fe30853c1a8516d9302ce26e40c8099a67c692235b98270f603286ae5c84d`  
		Last Modified: Mon, 08 Sep 2025 22:21:44 GMT  
		Size: 13.8 MB (13783580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5713fbd7efe3ca97c7d8b0f818271d1db37632535db2ed5dab595b814e74e685`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca1b1ce7ba77275f4de1d24e9266c9ee678cdcabee744cbef85850aa4af14d`  
		Last Modified: Mon, 08 Sep 2025 22:21:44 GMT  
		Size: 14.0 MB (14000848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbb6b6f9fa8f9ad902093c82331727e46d8dc23b71e24fcd060483df8f72ed0`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0733b2713b952be3857caf807a6c40eb4b80ec309753dd553b094c801eb52`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf7eb4717705271dd34326a04ab66650ac3cad5fceceee30d76bc2ac433ddc`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d88fe57081174796dee2c24b38044097eaaebf5e2378879460bb1a4d3b1e`  
		Last Modified: Mon, 08 Sep 2025 22:12:47 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17885363826384461a82888ef5f559decf5ab4bdda2a9a71a8913b239d2d2d1`  
		Last Modified: Tue, 09 Sep 2025 04:40:28 GMT  
		Size: 26.3 MB (26320331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41365a32f326d7412512c1e5e4c2056b81b35591ed6dfcbf77b1122cd3b636d`  
		Last Modified: Tue, 09 Sep 2025 04:40:31 GMT  
		Size: 31.8 MB (31808664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8342e15fb664702de7e2bb593212c099101eb5ffd46e37161a824ed02f2457e8`  
		Last Modified: Tue, 09 Sep 2025 02:08:09 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c8cc48027a8e879147f83f05b25d7b18ea55ba5fb4af82faeccfe878cf6a6e`  
		Last Modified: Tue, 09 Sep 2025 02:08:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04a6b3e2a66a9f00d2c1b66dfb2fa022bc2bace4301395b801be093ecfab78`  
		Last Modified: Tue, 09 Sep 2025 04:40:31 GMT  
		Size: 26.9 MB (26898590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994a53982efb5e28f3e21e03c9c12ff0226f0453981ef55b277fbad1993b365`  
		Last Modified: Tue, 09 Sep 2025 02:08:10 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d1f84fa311983c3915e52c3fb1ddb27127f5c7917d6f7bb9d68f5a600a7e1d`  
		Last Modified: Tue, 09 Sep 2025 02:08:10 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70420cdf6a5ece363bcc8d104d5540c0bb49f34862a95de9ce8658662a75e9f`  
		Last Modified: Tue, 09 Sep 2025 02:08:09 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:937a2a764f6e5e536e59d788a3aa3ac5426b6fe61002b6ba9dc546d295a64bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8296479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69c48e5a3f5728e03b9a3ab3c7d706253e9b1222c6bd1c72431e400240e84cd`

```dockerfile
```

-	Layers:
	-	`sha256:330935810565b4f27060b0c662608b3b631bf37ce1755e7706042d9f6b4a2078`  
		Last Modified: Tue, 09 Sep 2025 04:14:44 GMT  
		Size: 8.2 MB (8244308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0430c7b0c6423ac26b7a6a8e3058f9ab3032e222163a9d4743abdb4d78edc011`  
		Last Modified: Tue, 09 Sep 2025 04:14:45 GMT  
		Size: 52.2 KB (52171 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:1868f8a32a9928fa9b6bbfd0cd2e0ac2750e34949ac2b50f73b5176bf78927b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988b0957e43185ef8f9997d8572066be1297d0cd5d4cd6b92bf98451f4ddfcc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cb411c259f89ddfa2b2d033346731fa8204f13b8566958d0226a5c6480265a`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a63beb9ee6a3fdea07f8c32c3607d65424cdfb91ca8772eaf59d823fcdd9b4`  
		Last Modified: Mon, 08 Sep 2025 21:54:52 GMT  
		Size: 116.1 MB (116136712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9796ef33755d55869b309e8b523770eadbb6047e8d247abe2e5c0408f0d596`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1713743cdf04b37ca4990461e374020ef533ae184ab96abed5f99f87889884`  
		Last Modified: Mon, 08 Sep 2025 21:54:05 GMT  
		Size: 13.8 MB (13782931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13216c8f24cd0d92fb47da8778bd24fcb3e75f495f5747ec5923784a2b09bf`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d33d5d346369d7a5c6a0a92b5b3a180e7c2105cbbc205c46863e37739177`  
		Last Modified: Mon, 08 Sep 2025 21:54:12 GMT  
		Size: 14.6 MB (14635212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756c8f31b778ccabfd2fdb3b5f9828235efe859d42f00844636f2f9de876e4f3`  
		Last Modified: Mon, 08 Sep 2025 21:47:17 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0375f6d9ebb21e27d1c1c079186ac358237cdd01a1df533d30cc554ea3e9ef`  
		Last Modified: Mon, 08 Sep 2025 21:47:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c28d087a25847203d49ced394ba051be6137dc2a3bf0897c7d4c9fadd1d89b`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c689d46e36c029bf626b75695eee1f7453fe475596ec194285a003c48b686e9`  
		Last Modified: Mon, 08 Sep 2025 21:47:31 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6fb29e044627f97049267df09a36d066e87e284badfeb77acfbfbfa81e4c5d`  
		Last Modified: Mon, 08 Sep 2025 21:56:47 GMT  
		Size: 26.9 MB (26870953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f380455adbc9d364be9021a576811be245d607ba1abbbee08605d45b3131fad`  
		Last Modified: Mon, 08 Sep 2025 21:56:48 GMT  
		Size: 31.8 MB (31839446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac731a3c2597b892e5151b491e6335b7aff7c5c9563189f4d431507df4c3e02`  
		Last Modified: Mon, 08 Sep 2025 22:44:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a162a6661754da5232d6880dde4fa1243245595e477c7e12ee45cf3b208dbc1`  
		Last Modified: Mon, 08 Sep 2025 22:44:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a912c3d3a8a5b755040274353bbc06044afffab7e11c0493c5eaf824bf54a03`  
		Last Modified: Mon, 08 Sep 2025 21:56:48 GMT  
		Size: 26.9 MB (26898595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bf3e259740d61bf89fa5da45172fc5a134da639c42bb485e56a9ce33c8e181`  
		Last Modified: Mon, 08 Sep 2025 22:44:44 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e22cd7511667b441ca040e0f67e9456231acbd77aaa897a3105ed9dc9510387`  
		Last Modified: Mon, 08 Sep 2025 22:44:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce1478b5022ecdbe651517db61b2412064bac3bbdb6e3c1c01a2183755ad1a6`  
		Last Modified: Mon, 08 Sep 2025 22:44:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:7219366308317b679bd716210a6dfb194f604912c098110b3cf9cb60a58f915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8172865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a49749e7b5697effc7e26a2b364c400f689c13cb40b85250e0d3d33dd34ed40`

```dockerfile
```

-	Layers:
	-	`sha256:0f5439c9c1b2b46e5ef70c9cd0c2b69548c5bb6a3bd2aee61d0223a18d10865f`  
		Last Modified: Tue, 09 Sep 2025 01:14:23 GMT  
		Size: 8.1 MB (8120916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:379a821258f2473fd7c7256b13b07789d80cebaa1679b47b5900a7b2068ff2ef`  
		Last Modified: Tue, 09 Sep 2025 01:14:24 GMT  
		Size: 51.9 KB (51949 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:9b33d218498b84d0ea3057bbc5dfbe19b19cb5ad972152a9265a87f8a7cbdf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258795095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f687215312731939624d34d5085d847a732fb0da87974b8b7348c655625634f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03afb458e7def5cd6bc09cbac6e138c0d5dea54f31ce8278e16fdfea67a263e5`  
		Last Modified: Thu, 28 Aug 2025 18:17:53 GMT  
		Size: 13.8 MB (13796031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda77c7d92fefb7a8a2237a9df8a1e245fe8466b833ae549695035495fa3033`  
		Last Modified: Thu, 28 Aug 2025 18:17:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9e59c622efff7ff4425232bdf66a42838ce735df24a39a7a78b236d53001f`  
		Last Modified: Thu, 28 Aug 2025 18:28:40 GMT  
		Size: 14.9 MB (14884567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6305d9343bdfa79a34360a9a7ed43ece31c79af2f15ffb29b0e53d43726f0763`  
		Last Modified: Thu, 28 Aug 2025 18:28:39 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a5fe828b04be7a5867d24175a57781ac46e57b4d074b53f5401ccd891fd25`  
		Last Modified: Thu, 28 Aug 2025 18:28:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3a305fe26760566472326c944caf988756b203efa7bf9f487db665cc7b014`  
		Last Modified: Thu, 28 Aug 2025 18:28:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff18fb9d0205bcc99f3a3674aceb723a0a3cf7a0d872f8baca63977d88d05f8f`  
		Last Modified: Thu, 28 Aug 2025 18:28:39 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b730ebb92dcaa8a061c0091676274f75fed0edea00995c00293622d8521b056`  
		Last Modified: Thu, 28 Aug 2025 20:48:51 GMT  
		Size: 27.5 MB (27502599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f305afdfde8de59808b552b88aaa3180e6edd736f34b15fa3f75d1deca09a4dc`  
		Last Modified: Thu, 28 Aug 2025 20:48:56 GMT  
		Size: 32.5 MB (32505724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d736290cc7c60129313191b58cf08a3d4506968788c9f3bf829d77f46514d2c`  
		Last Modified: Thu, 28 Aug 2025 20:48:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438bea55a591afc069419e9f66c969dc867c5f49a00cccbf1ad053669e2cd03`  
		Last Modified: Thu, 28 Aug 2025 20:48:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4f823b3914140ccc37fd9bae3ad82f6ce54cfd6a270649f697752f264c33e5`  
		Last Modified: Thu, 28 Aug 2025 20:48:52 GMT  
		Size: 26.9 MB (26898592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064cbb16c5e31ce7dde35ef5f1d31c36dea522f558e3a898644a624a6712a6eb`  
		Last Modified: Thu, 28 Aug 2025 20:48:49 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959789e4ef6b6c410fa1b3d9599eed0dab8b8fc45e306dd2f59ad78f869892ef`  
		Last Modified: Thu, 28 Aug 2025 20:48:49 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6c106588afdc6e25b60d2c8d0e0eaecf51bcfa73fe7992211a0d26e9d27c6d`  
		Last Modified: Thu, 28 Aug 2025 20:48:49 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:81d5a00d9df2eb34a535532d13289d0a8ad344bab91354aeaaf679b848df328c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8199603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659997e5e34df527ff3c42063aab9a7f88fad5c8735a4ca6c3a8a60a2dda8fed`

```dockerfile
```

-	Layers:
	-	`sha256:25f4848aea3f24f88fa2e4f0de632642e45652ebd25ba7b4e624e0c27e6da7c3`  
		Last Modified: Thu, 28 Aug 2025 22:16:37 GMT  
		Size: 8.1 MB (8147557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b6791dea6ef856833c3fe63829043834d328d67c5bd6bcff6605b82138d165`  
		Last Modified: Thu, 28 Aug 2025 22:16:38 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; riscv64

```console
$ docker pull wordpress@sha256:36ac6bd7601c64074fc92131407451a2ef7242904d0850bad6d3fefcf3ed12b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285823142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcd77a552d478a04d3df972fbec5f64a4181e7c49fb5984e675332308cf93c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6f12b0240e0dbf97c8e4e7dcd68de87e0574ef0a3f23092d507469bd287a7`  
		Last Modified: Thu, 28 Aug 2025 20:15:17 GMT  
		Size: 13.8 MB (13795967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c460ecb1c90c1e778236105aed7163700500a98352ef0a0fc0ca5883f519ff`  
		Last Modified: Thu, 28 Aug 2025 20:14:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab17b9b790bddf7dbc628a33ccaaa51a8fdb34ef653212b7481dc6d44e8d57`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 13.8 MB (13823845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f5c3198a56e140882802698f7790c169e98cb53bf274bf7c65694b723be4f6`  
		Last Modified: Thu, 28 Aug 2025 21:22:44 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f819899f2a46b3af3292b9c55a3f827a8ea364a0db42778281293f7111043d5`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfec74d928323594efd185a50d2e951172758f7bfc69d5cfc30f4d5487d110a`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2762a744bb5ca0534b988987159d987b16547c885864469823acc4fa74f91d8`  
		Last Modified: Thu, 28 Aug 2025 21:22:46 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8906a7dc763ce0e81623aae2a430fbe366ebf4148c0b638ca7b5ada5bdd21c9f`  
		Last Modified: Sat, 30 Aug 2025 04:59:37 GMT  
		Size: 26.3 MB (26251383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6bc3c0c2155402fce3f4aaac010ddf4e0983da263400a5d04f49c6d20ca36`  
		Last Modified: Sat, 30 Aug 2025 04:59:37 GMT  
		Size: 30.2 MB (30185651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d434519dc25fbbd2f3d872b49835a93304f07e6a4059d52f7e220b5b6047fe`  
		Last Modified: Sat, 30 Aug 2025 04:59:35 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bec350db91bbe24807b02ab7a891d5c4662912166187794c9ca700c7118fea5`  
		Last Modified: Sat, 30 Aug 2025 04:59:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33621af506a85e0a36e6cced458e22e5b218783a5e166456bba388c365a4a845`  
		Last Modified: Sat, 30 Aug 2025 04:59:38 GMT  
		Size: 26.9 MB (26898596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8791e0d2490f93a1cbe29fdd31b829945433f16dfeff3f886cee6afae84cf7ce`  
		Last Modified: Sat, 30 Aug 2025 04:59:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5bb51e72a7cb34b626a3a14aac6c8bb216c5e3a2eb33ec27c113f12f71068`  
		Last Modified: Sat, 30 Aug 2025 04:59:35 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cab206e384e229f043eb79c9d2b39b2ecca084b5ec9bf7062d674010cab649`  
		Last Modified: Sat, 30 Aug 2025 04:59:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:13b23011fd943b479f65950b0ff8deb297028a470879602d731a11a710d28781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8270042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e18dc72c486fa5e9fe6999106540b5806aa9a31b951ad7471b3fe73121dd458`

```dockerfile
```

-	Layers:
	-	`sha256:587190b22020c9f369c1b05283e2ad7df60b5e0f1aefc539cf54bd8370819368`  
		Last Modified: Sat, 30 Aug 2025 07:13:33 GMT  
		Size: 8.2 MB (8217996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bed2331622988ce52fb5e3b859ada0e9daa8d855057d0d72befbc9c1f0e6da`  
		Last Modified: Sat, 30 Aug 2025 07:13:34 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:be43c36d4a7b04d9e9eb947c9e9381621dfd8036310aa22e2b50bade29473cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234492592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1d9066a293dabba73aecdae73680d8d9b5b7364309e7e6c0d1f4a8c9083af7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.12
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315b0bbaf3f0a13ecfdbc8198ee4184822abe3736eeae59551c67ca01981bae`  
		Last Modified: Thu, 28 Aug 2025 18:40:00 GMT  
		Size: 13.8 MB (13795360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d236682bdc44aa14a14c0c16c2ddffd676cdfada4136f07ec5aa43ea30d132`  
		Last Modified: Thu, 28 Aug 2025 18:39:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d475a13e5b71541d3ac9f574bf897e1c10038a0041f2b46316da8b455599fae`  
		Last Modified: Thu, 28 Aug 2025 18:47:42 GMT  
		Size: 14.4 MB (14447463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec833c1b5f56831890c15c5c313d3b5c93745f53bf2825340e3fda457876be0`  
		Last Modified: Thu, 28 Aug 2025 18:47:37 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f0c734a51821ec87501c5a097dac2225b18133d8df255e85636076f0489cb`  
		Last Modified: Thu, 28 Aug 2025 18:47:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caacda710f18b768f67d52640dc350491aec78d0fe56a05d60cb6949c73a8539`  
		Last Modified: Thu, 28 Aug 2025 18:47:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d40046ec192c0bff99f0f2cd969df02f48f4e0300b7d66709748a1037a03bb`  
		Last Modified: Thu, 28 Aug 2025 18:47:37 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebb7e50bdcaae6337d89613c6f065c0ec1369f2978b7b60c518b62ac384837d`  
		Last Modified: Thu, 28 Aug 2025 20:56:36 GMT  
		Size: 26.6 MB (26603804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed49d752b3c9fab1289a926ab93d920851de7f5f009c380ca9213eed945255`  
		Last Modified: Thu, 28 Aug 2025 20:56:38 GMT  
		Size: 30.3 MB (30334020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150b24e08fb3c0ecb79fc57341dd30274d6be50e60b315357d83ac848e39aa8`  
		Last Modified: Thu, 28 Aug 2025 20:56:34 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe45e8543b4ce5ebe97c649269011569594a5112dc04687f13ea1b116c3220`  
		Last Modified: Thu, 28 Aug 2025 20:56:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368cf115ad8ab8d5e236e5e9828ccdc1d50f1c1203c7be9f3290c12a8545d49c`  
		Last Modified: Thu, 28 Aug 2025 20:56:42 GMT  
		Size: 26.9 MB (26898591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc8431e3f068acb9d0b24d7cd2b5045241685dc92a3831eef0049457c77fada`  
		Last Modified: Thu, 28 Aug 2025 20:56:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7723852b89468561a9435cc107dc5d2a0a231dc9f8c5d2cbd0456306e29b5e5b`  
		Last Modified: Thu, 28 Aug 2025 20:56:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c88b963bd6853855887c30c95b82c4858ff6c2ca0d3057f2daff6dc4dd63d`  
		Last Modified: Thu, 28 Aug 2025 20:56:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:2c858fe2f8826d680ac7d193863f6b7f84e05ae9f2407682f6f7fe1e30378a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7923457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d2066d72881d2af55cd8e5d2c20ab939349a85d085c350a78ab6439964ca4`

```dockerfile
```

-	Layers:
	-	`sha256:54edf5ec6397b75b68e9360e7ec69457a687de9d1275273dba28a9d40a2d4969`  
		Last Modified: Thu, 28 Aug 2025 22:16:54 GMT  
		Size: 7.9 MB (7871474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d7f132cb1fdab05ad3804e5a344b40674ddf818862f34a27646183503a51c6c`  
		Last Modified: Thu, 28 Aug 2025 22:16:55 GMT  
		Size: 52.0 KB (51983 bytes)  
		MIME: application/vnd.in-toto+json
