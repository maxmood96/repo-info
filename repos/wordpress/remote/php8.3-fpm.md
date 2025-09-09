## `wordpress:php8.3-fpm`

```console
$ docker pull wordpress@sha256:7871eed556c8b34b0b6db16aea896dab13864c383c7292d980be4b6ef6f2b60f
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

### `wordpress:php8.3-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:d47d68d167a5dd1dfc68ea73db5363d70b818a2620e404c7304d29e869d227f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259473887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd60bb9b9abe4ae2c3b9c7c4257cfc3c96d673d8e61848a04ed1c31e13417bd`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:31705569600e8eccbe159daa449da1115febea148504de7e278d61bad581db21`  
		Last Modified: Mon, 08 Sep 2025 22:17:43 GMT  
		Size: 26.4 MB (26415160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c9071e57783533d1b68d2591e401860df090bbbb8b2ffc2ea4ae29e2a4b9e3`  
		Last Modified: Mon, 08 Sep 2025 22:17:44 GMT  
		Size: 33.9 MB (33908079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5d2f8fb0ceb02cd76bf414da4bdd9ee9ac6c8dd497b533a75d850ee1ad6171`  
		Last Modified: Mon, 08 Sep 2025 22:17:44 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a38cf953eb32eeb19edd5c73d62d45fcdce33a78b4516fc9a19b1e8d743d99d`  
		Last Modified: Mon, 08 Sep 2025 22:17:45 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43095ce156bdcfca97de996f8173cff81375cb431094491bbb689737c1e23f29`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 26.9 MB (26898581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98125d3dfa0d3f9af6b7f2182dcc7f65122eca037998325a35d25b429c68d806`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1176e645d6e8f6f268e771a5609a124c078d5ed59884907c26c9917209e65`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc140a48b4423609b620c18d31632b3346c2544fcc9448614ded8f56a98dacca`  
		Last Modified: Mon, 08 Sep 2025 22:17:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:57ab8dbbc3b6ce5efaec416e40c512bd19360b723585d0536f85f48ff7a8ef4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8199848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4233a2d13cb16b6021b9b5ffeb87a467fe799f965ab4f34c615e0b0dba68037f`

```dockerfile
```

-	Layers:
	-	`sha256:167d9c974e648dfab5006aca168080029b8ee5d1f0d1694bf7b24e7366258f8a`  
		Last Modified: Mon, 08 Sep 2025 22:14:31 GMT  
		Size: 8.1 MB (8147856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab17edc64f8bb8901f2ee12b76c2c2e0922bb3dfaade8e9424ecd2e4b58799ea`  
		Last Modified: Mon, 08 Sep 2025 22:14:32 GMT  
		Size: 52.0 KB (51992 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:e662c25dad05645d6a092e80bbff309e52343fe9684cce294af28f7e9e8cd134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229012015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ba604ed98355e4dfa6d0c1d25e6f4631f187164520e7df0cf8c1569e57f252`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:e449597fdf6cd80778b85400deadbf82fdf4ac7b5cf42672e5568f552231158d`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a21a095b6a9bf766a03a42e46869e4f15b3d708510ac992176caddb2a1dadb`  
		Last Modified: Mon, 08 Sep 2025 23:21:44 GMT  
		Size: 94.9 MB (94872631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da8dbd666467ca3bbf0c48c3d80944836ba10da741449b4a6a763189f0ded20`  
		Last Modified: Mon, 08 Sep 2025 21:47:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199b54e0fb123583829a17b52d0fd2d287731b826b9d4ac94ed3e9576468daf3`  
		Last Modified: Mon, 08 Sep 2025 23:25:24 GMT  
		Size: 12.7 MB (12728218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bd83028e20a91a22e2720d25b5677084bf0f1aca51615b0642978eb47c8e9f`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8df12bf375dd87bed23fe5657393326d74e8c53b5f6da57e16446f03bd063b`  
		Last Modified: Mon, 08 Sep 2025 23:19:23 GMT  
		Size: 10.7 MB (10686367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b66a4106e5a4119391c2f1cb0dc40dee8c0f72444c6780c9e601c76b5e6bf`  
		Last Modified: Mon, 08 Sep 2025 22:16:55 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28959f442325b6a78d4cf72f2b138c72bf71d3c0a01c3c05b590214a4eb58239`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd69ab3e4756050b5b89a09131db6ba24caafd251ab85da4efc2e164528633`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0b788ebe4aae53a5906effa548f2e04fdd1db2ca6e556f72c3a4e686c486d`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729b3fe49ef41d19cc035d75fc61ce42191e5552d5859f29c643498937e7b386`  
		Last Modified: Tue, 09 Sep 2025 01:33:08 GMT  
		Size: 25.8 MB (25835367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac53793387f11a086fcfa43baab789b475667b3f4d295dc3fe1eeb103409c58b`  
		Last Modified: Tue, 09 Sep 2025 01:33:08 GMT  
		Size: 30.0 MB (30030876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b15fc379db384e15d29f3c4bb2187a0c44e62e836596a9dcd2c637978e877f`  
		Last Modified: Tue, 09 Sep 2025 02:12:23 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c606b8d19711f672ffd3ee9aee870b99d3665755b5e23fd10de4c1f6aae9de58`  
		Last Modified: Tue, 09 Sep 2025 02:12:23 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801697f7971a4b89fd2968582784f068d7d3ea3163ef5e1342ed3a2b5718c6fe`  
		Last Modified: Tue, 09 Sep 2025 01:33:09 GMT  
		Size: 26.9 MB (26898587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c72856ac38ad7b4f922948c888d0dd7069b69ccaae92557aa7e9ba78f579e`  
		Last Modified: Tue, 09 Sep 2025 02:12:24 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6780ca79e3a13b439b96d8d68be9c59d01ad9c8265f45f7baea258141e807f`  
		Last Modified: Tue, 09 Sep 2025 02:12:24 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c329cd3e0e7e203625793a9dd294adcf4fc827a6b247665b522fad4c371ac`  
		Last Modified: Tue, 09 Sep 2025 02:12:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:2b4552d310afb03b1763320906409c5d396c2c9c44bf66402f722bbc38c2b4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7998970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f88cac19dcd2ea10c73022ef52bad251f20098286ffb447a7b3415450de8600`

```dockerfile
```

-	Layers:
	-	`sha256:f3fd31c555084e4a0b22703ab7fe5210882479ff7b5a34b720d7abc535aa1998`  
		Last Modified: Tue, 09 Sep 2025 04:14:03 GMT  
		Size: 7.9 MB (7946843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3352edd95229f29b4a58b54cd0e41be6b380577d19996380b5771e48cc73711d`  
		Last Modified: Tue, 09 Sep 2025 04:14:04 GMT  
		Size: 52.1 KB (52127 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:a4226b563f7f049ca82bd0ebb3f0999c715d550689e519ae362d177fb309a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215505388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34297a6771c5d50e463e94e289544b2ae5f15178f23b2538f1a57192e33075d`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:0068fad9f68032169424a79526da9a44bf9db7dd3a4dcac4a44a24293bfe6b21`  
		Last Modified: Tue, 09 Sep 2025 03:20:44 GMT  
		Size: 25.2 MB (25159840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e222da45cb6f5cf5004866c6b3adbba13ac63bbc67dabd94b05090f8f88036`  
		Last Modified: Tue, 09 Sep 2025 03:20:44 GMT  
		Size: 28.2 MB (28173124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f25fc21ee77ac2979ed434ab27ef0bcb0904b6ea24dd986b8b2d6a53aa345`  
		Last Modified: Tue, 09 Sep 2025 04:05:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadf3ef7cfb6ca486f34fe2cc033b72fbd50919297daf7bd3b7b987cb59468b`  
		Last Modified: Tue, 09 Sep 2025 04:05:35 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2336f52d3a26f17214002995851c0052694b48d0a2351787257d1356e4c37c`  
		Last Modified: Tue, 09 Sep 2025 03:20:45 GMT  
		Size: 26.9 MB (26898585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271979d6ff742012fd5d9471fb8a8e3f16ae90cc8bae88755e4349c72e0022a4`  
		Last Modified: Tue, 09 Sep 2025 04:05:35 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af3f1839a19df0796992a96fd0fe6026a0c506e4c47d85e185615ace068cd05`  
		Last Modified: Tue, 09 Sep 2025 04:05:35 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe305074e980552944b3d0d0e1c9fd64c7963182c4cf28c9e8114eccc14a1e`  
		Last Modified: Tue, 09 Sep 2025 04:05:35 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:450134b04359e035cb7f1f35a594a02993c4179d7171fed9929be49313df9270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8003770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74da65a5b26de57e908f16b34b8affe6cee78ed9afdc362ac643ac5c7c93944`

```dockerfile
```

-	Layers:
	-	`sha256:7baf80ee83396b92b8be094ada86a241f0189e3db1ad9a090d18da1d4f3302d1`  
		Last Modified: Tue, 09 Sep 2025 07:13:39 GMT  
		Size: 8.0 MB (7951643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ef237f7ca7b8e61cc3290aafde2da237be0d090c3ef325eb5e9006117d1658`  
		Last Modified: Tue, 09 Sep 2025 07:13:40 GMT  
		Size: 52.1 KB (52127 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0f584344a7e437618e7afdb3c49a0db11894b0cb111b997bd3c5feb0eed785aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249963910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23989d320f9f6144d8db1ad588b67c43531163689134b354315df1d2ff9ce824`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:8dc24ae3213212e219c43b38f985028fec3ce24374cdc2844f5d659cc0b18113`  
		Last Modified: Tue, 09 Sep 2025 02:36:45 GMT  
		Size: 26.3 MB (26320370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c685a1938ee3de0e3760545ad52848ff562bcba8357e8e923b003d34500d2a58`  
		Last Modified: Tue, 09 Sep 2025 02:36:39 GMT  
		Size: 31.8 MB (31777990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2a1e93183a6ecf0fd56c970f6769c9c77cf9706be2138eec70fd3449e2af2`  
		Last Modified: Tue, 09 Sep 2025 02:04:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cb84f8797b8e68e78860a052ab2ac5a15d38e2ba81fc077f58b960f27286f0`  
		Last Modified: Tue, 09 Sep 2025 02:04:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccefde55b013797318afd153d527d466c5c80e161db7d09bf718b809fe96e8bf`  
		Last Modified: Tue, 09 Sep 2025 02:36:48 GMT  
		Size: 26.9 MB (26898590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cfb1d6d16f266184d164d44bdc7b8bf1b3c44bffa04414016fefe1e1653165`  
		Last Modified: Tue, 09 Sep 2025 02:04:16 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2779786c9a3cdffebf06852626d79ea7b89aa42b05cc12de398f3e8932e76b`  
		Last Modified: Tue, 09 Sep 2025 02:04:17 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9825f485e4faa19481d953eb5c875b984d00a3d4f3e5d24bc12b59bd2f4ca672`  
		Last Modified: Tue, 09 Sep 2025 02:04:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:aef14388c6ea544d5a33e87cd8ded0f6b3de2768a1bf382b912d96da9935381c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8296479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48815cf6c55762183416e35f8c9fc71fe60a93e63ba4a825ac6a3816b694d581`

```dockerfile
```

-	Layers:
	-	`sha256:58fc1ac3cb7d9a8bbb42df8828e6032b1f5b5be8f3ea06a5a53f250a03e3b1f9`  
		Last Modified: Tue, 09 Sep 2025 04:14:14 GMT  
		Size: 8.2 MB (8244308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b94d95bfbad5f52eb634cf1e63f989b6ef3985c6721015946dc1daec8c19044`  
		Last Modified: Tue, 09 Sep 2025 04:14:15 GMT  
		Size: 52.2 KB (52171 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:bfabf520b9a35b0ad58df59101db120f19e8cea5ea6efd8f5fb40edcc0da1bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257848737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c141eab8cf388581df45baa24a17ec8c6e88ecfba51fb15e0b454a68f113313`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:02db201a82b667c271e097e3814099b5620ce07496c85a40c46b4641e1b3006d`  
		Last Modified: Mon, 08 Sep 2025 22:32:32 GMT  
		Size: 26.9 MB (26870962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ede2d6457ea5ee28e810e031ffdc420039c9b6e47e541189d90f397e8f8fa73`  
		Last Modified: Mon, 08 Sep 2025 22:32:08 GMT  
		Size: 31.8 MB (31802743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab38ee3c04a1bf255c0ff1414a5d727779b32c72261eb34284335df2913c64c`  
		Last Modified: Mon, 08 Sep 2025 22:32:14 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b201a015d920350a5c65d42611b71cb9db18ca4531988d953507818160fdaa`  
		Last Modified: Mon, 08 Sep 2025 22:32:17 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb23e41c360e271233c0af623349706b134e76ae0569eba7faf8e389e0d9745b`  
		Last Modified: Mon, 08 Sep 2025 22:32:12 GMT  
		Size: 26.9 MB (26898582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f964bac6e858e74c4771d1816dbe5c48c0b6151f7e6e79770010fde2f835d19e`  
		Last Modified: Mon, 08 Sep 2025 22:01:39 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fff038dbf7d5b2a186b0ffdb45d5670ebf0e5857d1bad0148639d2803bb70b`  
		Last Modified: Mon, 08 Sep 2025 22:01:39 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623f0fbe79d994918d6eea7e6e704b1a644e54eecc668422284f38ef24c2ecbe`  
		Last Modified: Mon, 08 Sep 2025 22:32:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:fef4b5c7259cdf346c10a11a4a3825bf6daee9293e35a1e09e3bc7ddd15f67aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8172865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6340360172ad5733893a0192d4852a1d7c1a3f8e89db7782eaa8fc8af3838ef`

```dockerfile
```

-	Layers:
	-	`sha256:60c568b881d120c0ac9927eeb6d338d7b764d244ff8a9c30d28e8d4c31d55dfa`  
		Last Modified: Mon, 08 Sep 2025 22:13:45 GMT  
		Size: 8.1 MB (8120916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d6ddff0bff476297fc6f7b78e6dd0bb931f5113696594a15c094d7d0f1e960`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 51.9 KB (51949 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:dbee55ffd10ff7666307dc2ea8d5fc215f28dfd1f5840c706b59acbbc91b0c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255261146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cdda294e8c088a706b88f3aa78d8361c742b76bab552a13d8505e017cc145a`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:0debc761f2d6593ea4a2e084589668d2dcde5860edf1ea69bf7908835582642d`  
		Last Modified: Thu, 28 Aug 2025 19:22:35 GMT  
		Size: 12.7 MB (12743308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fea9443ab7287ecc25d8af7c47f1a959cc060dc26e2e9b34ce0af2412af4b7`  
		Last Modified: Thu, 28 Aug 2025 19:22:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d82f7a64271fd8002c553022140d8c6cc968b87a1456565062fb37f68d5728`  
		Last Modified: Thu, 28 Aug 2025 19:31:44 GMT  
		Size: 12.4 MB (12433869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59bb784ea031cb0e1870efb1aeae5037d9a8fa89b3d0e25453dff7fe0d5b1d5`  
		Last Modified: Thu, 28 Aug 2025 19:31:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27a1380d4498a154d552b0497f1ca8ae131483f8cdf36ab577f8dad1ef6c3e`  
		Last Modified: Thu, 28 Aug 2025 19:31:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9f784c279da174c7d1705b6c9ec0849ed58ff322e06596b29cd32ccd2ad62e`  
		Last Modified: Thu, 28 Aug 2025 19:31:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50f2cf025cb7db63b69737fa86a9844b91305a864f8e7fe303e90b74e235f8`  
		Last Modified: Thu, 28 Aug 2025 19:31:32 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5d63fd87e975462202ef088e18d4606f3c3116565a6bd87466096c6fe39215`  
		Last Modified: Thu, 28 Aug 2025 20:37:03 GMT  
		Size: 27.5 MB (27502618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0540bc0798e8014a5af76dd40a2608f17a88d520459a117841e204a4b46811e4`  
		Last Modified: Thu, 28 Aug 2025 20:37:07 GMT  
		Size: 32.5 MB (32475190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044dee12023ec9b98a056e9b7dc1e01699305eb16eef1e57dffbb0e42283a3ba`  
		Last Modified: Thu, 28 Aug 2025 20:37:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52a3e5e9ec33c4c9791cbfae8b539a1532cc8f51769065342bafd6269208ead`  
		Last Modified: Thu, 28 Aug 2025 20:37:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d3a58114ae57e772680a858ab2c2c3b9c618e04029e7de02158bddb79964a`  
		Last Modified: Thu, 28 Aug 2025 20:37:06 GMT  
		Size: 26.9 MB (26898595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e32d69571dac0914be5722104becaf0918d27bf8e5afeecb0bc2987d7f1a46`  
		Last Modified: Thu, 28 Aug 2025 20:37:00 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f41a4c4ad077970194046441397d9c162614a5c880d76e1820b85fe3231c3c`  
		Last Modified: Thu, 28 Aug 2025 20:37:01 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4afc48eb3b5135e20bafa9268e54f246a9ef8423e6318c0adac015675497150`  
		Last Modified: Thu, 28 Aug 2025 20:37:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:0f7d77b256a1e06a45d8eca1e348907cc52a7bd99451cede5a50560bad1b1e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8199603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65ba2bf7bd08266d6ef62987862b508b8994114bdb3f115a9c14d6d0fc1b529`

```dockerfile
```

-	Layers:
	-	`sha256:dcb2b0edb65d8b0e41c5b1b8473b6b202467ed6c86c759145e11b45b6b9146b2`  
		Last Modified: Thu, 28 Aug 2025 22:17:29 GMT  
		Size: 8.1 MB (8147557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418b72257bea00204a4c329cb64cc1fdfc4ccc71b389cc5779841ab7c1737234`  
		Last Modified: Thu, 28 Aug 2025 22:17:30 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; riscv64

```console
$ docker pull wordpress@sha256:5c27dc4a0451aa89c6bd32e96604ad4ccb92d7d98d58bdc1ed1a23eee5947522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282367555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1974828b5f14575ebaab99f4fb9e96c2fbc3f8a02d686e3f0e5dd4480560377b`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:5e77da6d6e964c0fa82cc132ef69665803cbe00bf2445bcc0890ba7ae11b00e7`  
		Last Modified: Fri, 29 Aug 2025 05:06:41 GMT  
		Size: 12.7 MB (12743271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b2e2338b874b719ccb220103b416aeb84140098fa1254b9ea842f29f7e2b56`  
		Last Modified: Fri, 29 Aug 2025 05:06:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf87fcf70a98b748a9a6615ad675002ffcd572f6862a967fe466f93bc74ad5f`  
		Last Modified: Fri, 29 Aug 2025 06:53:43 GMT  
		Size: 11.5 MB (11459811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6a2c5c29c1d7dd9fc210f0ff04737d1c5cbe4bbf66af8ce4955cd98b441977`  
		Last Modified: Fri, 29 Aug 2025 06:53:42 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305311db957b0b65478f7d566c1be700d915409005217ea7b3f359df8905216`  
		Last Modified: Fri, 29 Aug 2025 06:53:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cefd6dff4c1e1573f76b15202cc2a06c90684c6b36629c7bbed6c75eb6b5c1`  
		Last Modified: Fri, 29 Aug 2025 06:53:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9eedb2ad3904dc601de00e39afded057885c0a0051c42f95f43b4eaa05dfbaf`  
		Last Modified: Fri, 29 Aug 2025 06:53:42 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f09689d0988ff9993978a528f4a01185cc0786c422c65dec3c8842e627ecd`  
		Last Modified: Sat, 30 Aug 2025 03:52:48 GMT  
		Size: 26.3 MB (26251513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d15ed7de528445514c7b450e333c9d8a4239e1d1a93a6a484914a7ca722e37d`  
		Last Modified: Sat, 30 Aug 2025 03:52:49 GMT  
		Size: 30.1 MB (30146677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71677cf4dd2098086339cac013c875516ca3a3a79be79a96ed45da3558d8cc7`  
		Last Modified: Sat, 30 Aug 2025 03:52:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d5d34a877f8a923b45ed1b2930f8ae349449a7d9a5cdb4b6bcc3e76490b359`  
		Last Modified: Sat, 30 Aug 2025 03:52:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a54ff6ac9108c304c5572af5af239ff1b6b5f22eb479193617ac68a51356a24`  
		Last Modified: Sat, 30 Aug 2025 03:52:49 GMT  
		Size: 26.9 MB (26898596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd9fa81a26ad46f82cbbb05e56ca483b6d26518dbc0229f85b71949b1731e64`  
		Last Modified: Sat, 30 Aug 2025 03:52:47 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f951c73011c0d652a329c1f3b015de92f422c1b33f8f74be2030de64a9bbcef0`  
		Last Modified: Sat, 30 Aug 2025 03:52:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0733a0c781f61ab606320b1918474cedfe105c44658b5a2735884e9bd56bc5`  
		Last Modified: Sat, 30 Aug 2025 03:52:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:e020328c80e55351a4a3e17ca7663a719d1887d0845594bd9e26a27aa85e8421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8270042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4ccf744bc10f32834f31ad22df0959c07bc8d8443a2dd4265d0223e9a789a`

```dockerfile
```

-	Layers:
	-	`sha256:344bb0d2a7455f2401ca47a32cbaa9f71181ff63d52751e43690d7f3bd20153e`  
		Last Modified: Sat, 30 Aug 2025 04:13:12 GMT  
		Size: 8.2 MB (8217996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da89060e00e805678e74c70c9a5d1d284d38500d3f3d800b6da1420a558368a7`  
		Last Modified: Sat, 30 Aug 2025 04:13:12 GMT  
		Size: 52.0 KB (52046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:a2b008b3a8f97b7d663f6830a0a57adad308d758850f6fda12a64ee0c86148a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230720490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a29552914ff6b9cd7a9ece7bd3604b53b01fa7b2d4cfe72a66933c95c803b98`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.3.25
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
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
	-	`sha256:ed64eec1dd20ed1be23225dc4edb20e89e9ad2c83e8b355777de06e9e6fb2286`  
		Last Modified: Thu, 28 Aug 2025 19:36:55 GMT  
		Size: 12.7 MB (12742704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09541a475b5619e6fd2464a98a4e80bd190d418a92bd4f7e52342d2c956c214`  
		Last Modified: Thu, 28 Aug 2025 19:36:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2e9baad25fc9d2152bea4985ef4e4b57817bd8a70a6b093513d9357b653e19`  
		Last Modified: Thu, 28 Aug 2025 19:44:04 GMT  
		Size: 11.8 MB (11763220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf1dea39c2cdeb4ce3d4c06c783cca547509fce527b0112913e51f2a15db4a0`  
		Last Modified: Thu, 28 Aug 2025 19:44:03 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eeb7792772d1f0fa865d108dbf61e30cd726af7234e45417f086ea1b2ef305`  
		Last Modified: Thu, 28 Aug 2025 19:44:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e416caf1e1c764d2693cf0a2d153b22b204bcb21c184cf9695a4c8bdd45c7e`  
		Last Modified: Thu, 28 Aug 2025 19:44:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea3bae9df0381552c6e622a46fd73d2a4031dde76fa2c51d050b92ffe58221`  
		Last Modified: Thu, 28 Aug 2025 19:44:03 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cdf82ac28d7a64f9250e2208c6bc1fb4b100e7a6d8e8966be808f9d6edac7e`  
		Last Modified: Thu, 28 Aug 2025 20:51:34 GMT  
		Size: 26.6 MB (26603851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c089313d02b85a17ae6446dd3091b40c496e40ffcc96cff658a1440d75bde8ef`  
		Last Modified: Thu, 28 Aug 2025 20:51:35 GMT  
		Size: 30.3 MB (30298783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235fe9c17074bab5c46b8122f5cfe9e26c543bf1030adca9dcacaafa2539cfb6`  
		Last Modified: Thu, 28 Aug 2025 20:51:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7307de050d796aa29d016b95e65382848800caa92b2ff1dd516c3adbeff02f76`  
		Last Modified: Thu, 28 Aug 2025 20:51:32 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30e2b9dc6dcd8668aba6cf3c7e4e06f5ab0dfce1dabd05dd7d8f06c1cf30f2`  
		Last Modified: Thu, 28 Aug 2025 20:51:35 GMT  
		Size: 26.9 MB (26898588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e73f2aeb94e0b68527c77809c82d3a6f632f4f18c59335712e97477e282df0`  
		Last Modified: Thu, 28 Aug 2025 20:51:32 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c86be81515da7b267751392bc6e25fe5899a5ed1f591f2e0c7fa152dbceb4f`  
		Last Modified: Thu, 28 Aug 2025 20:51:32 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1cfa4c6e0fde694e28275dc52c7c7144d46b2ea551c61399bd0f6abc916838`  
		Last Modified: Thu, 28 Aug 2025 20:51:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:3fc4a9615226789e5ca674000d1b61e84703f8d2f2102e924da86a7faf7bcef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7923457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13de3edb4d147caf36ed076e8241e176211551c7c3b5187c8dadba4f408b94ad`

```dockerfile
```

-	Layers:
	-	`sha256:fc0c874b938f6f5d1294091a6c3159c38c91c14159a660726a8b8f558c67a2a4`  
		Last Modified: Thu, 28 Aug 2025 22:17:57 GMT  
		Size: 7.9 MB (7871474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bd20e2dcbed10e3dab0eadf2ce3a670f58c4c152583ec1428930f11ed6c371`  
		Last Modified: Thu, 28 Aug 2025 22:17:58 GMT  
		Size: 52.0 KB (51983 bytes)  
		MIME: application/vnd.in-toto+json
