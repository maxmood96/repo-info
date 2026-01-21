## `wordpress:6-php8.4-fpm`

```console
$ docker pull wordpress@sha256:cc6a0d62b1379e7715d655f03f203dee86b4e078d408f8645ff5e9f5a7f96bbf
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
$ docker pull wordpress@sha256:1c04f77d7dc4923596a5c5a8f22d3f664454850012a09f5af7dbe7c9a39eb33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262512470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b676cd1d63539778a39904db1677c28356be2d1f0d19fba36002fdb26a8d80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 23:11:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:11:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:11:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 23:11:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:11:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:11:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:11:46 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:25:09 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:25:09 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:25:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:25:09 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:25:09 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:53:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:53:50 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:53:51 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:53:52 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:53:52 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:53:52 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:53:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:53:52 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:53:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcc69194de6bdd46a1044d58a17097b0f896a5c11584a8d3f9d207532c5409a`  
		Last Modified: Fri, 16 Jan 2026 23:14:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b931ac6d0eec33ba91b9308176d0011f9563d19dd356ce1c16619c922f8143`  
		Last Modified: Fri, 16 Jan 2026 23:15:18 GMT  
		Size: 117.8 MB (117839374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ff79a09c661cc013e50f57bfeb26cb2dfade62417644985424942690ffeb7`  
		Last Modified: Fri, 16 Jan 2026 23:15:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc03ed0f80cf256f9cd8f6c862f3c5e23567efaa44b7acc4835aebe12802111`  
		Last Modified: Fri, 16 Jan 2026 23:32:54 GMT  
		Size: 13.8 MB (13817894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f7ab3a74119a7bb97508a425259d6fb5da69b6c75b36d3a2b516dd1b2a35f4`  
		Last Modified: Fri, 16 Jan 2026 23:25:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8189cab2bac6de452592646936435e1107cb81571b81efd0a69b38be7addba`  
		Last Modified: Fri, 16 Jan 2026 23:32:56 GMT  
		Size: 13.7 MB (13670175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8ea236d0b2d1cf8aadd471fba2b2bfd698bd0341eb8bb3b00945ca107dee33`  
		Last Modified: Fri, 16 Jan 2026 23:25:27 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e46df0b82033d7a37e5815b6e95268db1e761cc3d9241b03459a7f443b03717`  
		Last Modified: Fri, 16 Jan 2026 23:25:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f298265f069bf5c972b4f53178b7de1699480f8fe1779278fc43f98ed658c057`  
		Last Modified: Fri, 16 Jan 2026 23:25:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201150902884c675c57660520dd3bb01073d6af6e9e6bd2d4bc5d78048b3aa2`  
		Last Modified: Fri, 16 Jan 2026 23:25:26 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158581dd6255fb7f6c5392bb450c7b25fd7d95431048f049eaff612a4142e9bd`  
		Last Modified: Fri, 16 Jan 2026 23:54:15 GMT  
		Size: 26.4 MB (26413803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53129a0100403917789d9aa8aaec4a196a38091dc160ace779e6e5d04c876909`  
		Last Modified: Fri, 16 Jan 2026 23:54:07 GMT  
		Size: 34.0 MB (33954589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e46c38cf9a01789b3d6ff48350ca418aed778f520dab5b73b25634a17d698c4`  
		Last Modified: Fri, 16 Jan 2026 23:54:12 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfbe8be80f566f6297982265ddf4ac2b89a076e3e2931603fa2285e4e35c5f2`  
		Last Modified: Fri, 16 Jan 2026 23:54:12 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1e7647ed108e4e83f8c78169e1141966f226baada9c71d6d61e1854b1e34ae`  
		Last Modified: Fri, 16 Jan 2026 23:54:14 GMT  
		Size: 27.0 MB (27024655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca167aff5b9ad7202fc38523be2ef7a9c2c19e0a03671b5d0f577e79dd6e0ab3`  
		Last Modified: Fri, 16 Jan 2026 23:54:12 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76409fdb35b6d9b0ddc68e98a13f06a64898318699b23525ced02280af160009`  
		Last Modified: Fri, 16 Jan 2026 23:54:12 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8facc8cc07a24153dbbde722793a5116098a472787ebd2f79fb3092522666782`  
		Last Modified: Fri, 16 Jan 2026 23:54:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:78654f97cf15943e58597dd7017b7bac64f05823591e9936d336ef355b8022b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8200503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633e7d30d639f5096c6c8fe543c05f9c1da09375aa16f580864ba0b3334cfcfb`

```dockerfile
```

-	Layers:
	-	`sha256:bd0690b2e24e72237bd202107358cff6428bd2828dd69b4bdd41e8c371a67acc`  
		Last Modified: Fri, 16 Jan 2026 23:54:06 GMT  
		Size: 8.1 MB (8148503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2e3c59eb02fc75b6f7e59c800961568414e06afdd91b8384658c7744e154fa`  
		Last Modified: Sat, 17 Jan 2026 02:14:57 GMT  
		Size: 52.0 KB (52000 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:279d5fbe626abdac3f5eee57dd5471a736dea016bda00b0a9b3e64f5d7d1a02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231823687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc228a60467a0b88a68bb38044eea44edc724c158fbf9397323f380788f866`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 23:28:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:28:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:28:37 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:28:37 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:28:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:28:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:31:45 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:31:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:31:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:31:45 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:31:45 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:47:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:47:21 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:47:21 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:47:23 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:47:23 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:47:23 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:47:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:47:23 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:47:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86220f95b2f011b74bd0cf112a5be7a01adc96a11ac61f102513f987c7010150`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6189334351d9f45e0af8eed80035414defb889775a1f1869a8410f89e885b4`  
		Last Modified: Fri, 16 Jan 2026 23:32:06 GMT  
		Size: 94.9 MB (94876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadde203f0852e4cbbc907f7bcef625611eeb51db0fd260da8af3b45df750ed0`  
		Last Modified: Fri, 16 Jan 2026 23:32:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c256e599f47718608d58ca924b0a1bcdc5bac3f61aa3912e5736f130f642d671`  
		Last Modified: Fri, 16 Jan 2026 23:32:16 GMT  
		Size: 13.8 MB (13815482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039bb03cb1d7125ab69bf743fb3bf9cfa8e1cd292cb6f316092a0df876252d93`  
		Last Modified: Fri, 16 Jan 2026 23:32:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b89be1c09e120561c4a2d1da54fffb8a7f969b54d1de197a6dfc1bb8ac8bd7`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 12.2 MB (12238030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741938b732fa5e2996f922efca90a97909d578d442a2ed41982243b5e8e67c7b`  
		Last Modified: Fri, 16 Jan 2026 23:32:16 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef185f13d669c92f7e4ba29f5b0b778d88ff5128d45571f9731a10eeb31d10a8`  
		Last Modified: Fri, 16 Jan 2026 23:32:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4e79c22414e7e09456f7b9cb29d5ca88a8c41b056db3caadcf12d43c0d9b2`  
		Last Modified: Fri, 16 Jan 2026 23:32:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db4cbb785ca45b8bf7685b902189a7ec63f864e58d9976ef186ee6792d95d9`  
		Last Modified: Fri, 16 Jan 2026 23:44:29 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9741784e22de5d1e809142f6338e7617218726dc4fc95f18e4759fa4946b889b`  
		Last Modified: Fri, 16 Jan 2026 23:47:39 GMT  
		Size: 25.8 MB (25837097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d68a4ff020ab6f7ba41aee4f81d7bc8ea17c05c54fb8df9e4d8e43fedd2481`  
		Last Modified: Fri, 16 Jan 2026 23:47:49 GMT  
		Size: 30.1 MB (30070755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6481056c980b63678aa548b060c031a05fc46bdf019e0846bba9c028820731`  
		Last Modified: Fri, 16 Jan 2026 23:47:45 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff0150142cbdb8466f92aab3c5396ec5ef67f68fb6bed79afc1812bdaa75797`  
		Last Modified: Fri, 16 Jan 2026 23:47:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e9f08e654cb1cb360d9d82a225cc04d087434f974c85435a57b4a83eeb1f8`  
		Last Modified: Fri, 16 Jan 2026 23:47:50 GMT  
		Size: 27.0 MB (27024656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb57bcddd87eebdcf681b02ddf953766d001ec0f7bb5b969b431b914410ee068`  
		Last Modified: Fri, 16 Jan 2026 23:47:45 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f6ea2c8eb91f2d2ec3d99f22ee04946f7852b8b7b896c91a8f06a218fd4dee`  
		Last Modified: Fri, 16 Jan 2026 23:47:46 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b0c27270f60ecde93654a721e3eda4730c2f7dc45bfb169760759c55bf3d7`  
		Last Modified: Fri, 16 Jan 2026 23:47:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:9194ea27adf991898b54e43d21fde646598040a6495c374db934a9938608290a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7999626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f2b50b0196296977f29b2752e20364070e2fb06aadaa9ddf2786271b96a17a`

```dockerfile
```

-	Layers:
	-	`sha256:32694115bd2d872e1b7f09c98afc6be5141a105b4736fdbe332d6881b5b30884`  
		Last Modified: Sat, 17 Jan 2026 02:15:05 GMT  
		Size: 7.9 MB (7947490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef84d0cc9d8480c5f80d1e408189d7ace395ec703bf8086719aa26bcbee72f`  
		Last Modified: Sat, 17 Jan 2026 02:15:05 GMT  
		Size: 52.1 KB (52136 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:26cd737feb0950c4897808515d906fbc64a2ee9b9d57cf462737cd8e81f2d4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218238944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cbe5876f11aa065a49c5a0d70dce62f4fdf2eee461b0460facfedd31ceaab3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 23:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:32:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:32:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:32:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:32:51 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:33:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:33:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:35:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:35:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:35:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:35:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:35:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:35:41 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:35:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:35:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:35:42 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:35:42 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:49:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:51:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:51:32 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:51:32 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:51:33 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:51:33 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:51:33 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:51:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:51:33 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:51:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70c07e6cee5f648e9ce973e8cfc5aa47036b644327adfb3d9c69b4446c821a5`  
		Last Modified: Fri, 16 Jan 2026 23:36:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a23010067badc71dd4b2db5a0e569d81056787814e6aa31ea6f7b890587db93`  
		Last Modified: Fri, 16 Jan 2026 23:36:14 GMT  
		Size: 86.2 MB (86244620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bd77a891e76f5db39583ab8437d22140820124c93efdb6ed08dea5c3f779b`  
		Last Modified: Fri, 16 Jan 2026 23:36:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a169a3a103a84f651bdf0f4b7ed460cb3fbda7824fb2d9dc6edbff9c78189`  
		Last Modified: Fri, 16 Jan 2026 23:36:11 GMT  
		Size: 13.8 MB (13815564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2475c5dc60b49720c84520ef7226217773723b2dea9088d710962b03228ea2b0`  
		Last Modified: Fri, 16 Jan 2026 23:36:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eb44c1daacf1330c15633d99598bf78c438154b02a116f781e26c7421ad851`  
		Last Modified: Fri, 16 Jan 2026 23:36:00 GMT  
		Size: 11.6 MB (11563306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d99c016ff034e7a3822e0c3fe604fad45cca062bf8cf73808b849a51b3e5984`  
		Last Modified: Fri, 16 Jan 2026 23:36:07 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8ab86307460fd5c41c38d5549242d9f3b94c398e698893930fcb70d3fa7229`  
		Last Modified: Fri, 16 Jan 2026 23:36:00 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab17e00b474598176ce0561e24711caae1462c8eff19eb4ce5fcaa4258d339`  
		Last Modified: Sat, 17 Jan 2026 00:07:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c392f49e371195cd996837ada981943e0e9fdf6fd6dfbdcb486a5cc9ffc8d30`  
		Last Modified: Fri, 16 Jan 2026 23:36:01 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c8cd55ddf97722effc5ed4cf1eb05780b25dd7bace4469274cffcf169c5ce2`  
		Last Modified: Fri, 16 Jan 2026 23:51:48 GMT  
		Size: 25.2 MB (25158427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d66a96059e2abf0f3224ff79b7b31ee38d3be26aab8341bfba3ce302878a97`  
		Last Modified: Fri, 16 Jan 2026 23:51:56 GMT  
		Size: 28.2 MB (28205497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083c4e4fa7e183153153f7b987a3314669db5199781bddc1fa57aad1804e442f`  
		Last Modified: Fri, 16 Jan 2026 23:51:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4409f920c41997aa6612602f3ab2800a5820f1bf99a2e5e1c210d36c840762d5`  
		Last Modified: Fri, 16 Jan 2026 23:51:55 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e197fa249b0f90abc834ac5f46e6c9e44b4288901022be20cb28c619d94fa1`  
		Last Modified: Fri, 16 Jan 2026 23:51:48 GMT  
		Size: 27.0 MB (27024644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7786363a07fa45bad5f253f287fa79c4a0d8141c90230a258b3e9ac85a7656c1`  
		Last Modified: Fri, 16 Jan 2026 23:51:55 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947785039b03bec98b8939086c2ae0cafc0a41a56a0f169aa05935bbdfd07ca7`  
		Last Modified: Fri, 16 Jan 2026 23:51:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a04d5880447e75a26b67c6b9d1b216b985a9381c5c91d36a05d8b73ac97b824`  
		Last Modified: Fri, 16 Jan 2026 23:51:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:8f19d84ac43b37523bfde69536fa7e26eee3b2c31ee0dbcd133815e721decc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8004426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f94ba938912a8581adfb1646e9095cc6e5b3161a742e66c82ee563ebd84a18`

```dockerfile
```

-	Layers:
	-	`sha256:1af045971ce6efd37edd8406792d236b840c4815efa0652b0846a192c044693a`  
		Last Modified: Sat, 17 Jan 2026 02:15:12 GMT  
		Size: 8.0 MB (7952290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1df1bf0bb53a979beca6723d368b4ba3ae7dd3b7836cedfd2a80783d90a8344`  
		Last Modified: Fri, 16 Jan 2026 23:51:46 GMT  
		Size: 52.1 KB (52136 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:64a8e1f27c5d70d5e576e48f38bbab6af804e0f0063ada1fbd5971f8ad1cbf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252621774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd4acd9efa0da59a4956835fa07b5667c550326ef2fd6fc4bb999bdd438151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 23:17:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:18:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:18:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:18:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:21:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:21:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:21:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:21:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:21:12 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:21:12 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:21:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:21:12 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:21:12 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:34:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:35:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:35:46 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:35:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:35:47 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:35:47 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:35:47 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:35:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:35:47 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:35:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:35:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17ed878f99a8cd5e8b93355ff4f32b79eb661fe0044fa342e00707a9d02035`  
		Last Modified: Fri, 16 Jan 2026 23:21:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282a2cc39cc73464fd990d3d1559cf518addbee90cf825affc007bb3cc411cd0`  
		Last Modified: Fri, 16 Jan 2026 23:33:58 GMT  
		Size: 110.2 MB (110164047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6042169ac4ed7137bada1974d77a710608cb2093d686b45b10b8c657e89cf8`  
		Last Modified: Fri, 16 Jan 2026 23:21:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf96237b2b52cbcf15232b63674840c8843ab33a9c0302bc12ebf38a002b010`  
		Last Modified: Fri, 16 Jan 2026 23:21:42 GMT  
		Size: 13.8 MB (13817489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a380c94c576af1ee6d0663ae23d353a44167352ecef62008436debf845c5b3`  
		Last Modified: Fri, 16 Jan 2026 23:33:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b5c3004b3fd7011c7b709e483038928002fb7fca73dc3ab9688aa08198ddd8`  
		Last Modified: Fri, 16 Jan 2026 23:21:33 GMT  
		Size: 13.3 MB (13334152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1386da206fd6cc1858888b37b3104e1c99eec92726a0e831daaaf9c8992950fe`  
		Last Modified: Fri, 16 Jan 2026 23:21:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cd92bd78cde3f0309fa826029cd93e73288fe03103c6d82d2c9c7db03957db`  
		Last Modified: Fri, 16 Jan 2026 23:33:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6810faf5e4bc50385b7090d490e009f968498158a52997097b95065eca03a`  
		Last Modified: Fri, 16 Jan 2026 23:21:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840dd870aaf0a2bf6b62795daa264a513c3edc2f1b458ea75edb0228a362c5d1`  
		Last Modified: Fri, 16 Jan 2026 23:21:35 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7b037e89d100fc6831e1c98285fc866653d38fec70007cc815fb2b34a10154`  
		Last Modified: Fri, 16 Jan 2026 23:36:13 GMT  
		Size: 26.3 MB (26319952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34fd0129c2fea932e1b4c6594b0572f7805cc90fe456a00f22daa81c6492e82`  
		Last Modified: Fri, 16 Jan 2026 23:36:13 GMT  
		Size: 31.8 MB (31809107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d84c313b299b3f6eb6288aadcaafcd552ba8f95d520ead1c8cc4c0eadf9b1`  
		Last Modified: Fri, 16 Jan 2026 23:36:03 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b5700b7208b507493785033c5d3964e3f62a4ee133d62e56636957934ec857`  
		Last Modified: Fri, 16 Jan 2026 23:36:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc755a19c58b166aa7847ea0129b82a969699045b605da3337b894897a2071`  
		Last Modified: Fri, 16 Jan 2026 23:36:16 GMT  
		Size: 27.0 MB (27024681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecaed30d0f26f56bcb3e386654892683737f55969405def25b7df5dd0c97246`  
		Last Modified: Fri, 16 Jan 2026 23:36:11 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcda9b3737aa42a6cee9f5b3b45f0dd3f67b64ac9597c72a078766a757324a8`  
		Last Modified: Fri, 16 Jan 2026 23:36:11 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4a4a8f43ec6ba9e2fabf32814580dd9bded6949e8ead07037a2d898066cc57`  
		Last Modified: Fri, 16 Jan 2026 23:36:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:d1fca524e07d044ecd8d8c5eb4422645a690951b014bee19b7931560cd59b8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8297134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a5d404c0e5dfa6250a5c9e8ceb91e5aed83627b122ebc02e3ccfffe1c0a6b3`

```dockerfile
```

-	Layers:
	-	`sha256:831d5e6b605c42eb23ae3e93fe8492fb9bb379d8e21669d6ff35055b00ac9fe2`  
		Last Modified: Sat, 17 Jan 2026 02:15:20 GMT  
		Size: 8.2 MB (8244955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e51bcfd35f8774e49d16807f51194949dbff4f99bd6b43029df2d0f71bf9575`  
		Last Modified: Sat, 17 Jan 2026 02:15:21 GMT  
		Size: 52.2 KB (52179 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:249e8e392b6a6cd8faa1366819b39fa4b2f530e8f8f0c3df7d24c6a41df2711f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (260974855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523eb851eaafb429b0f097adc6068fef0790eb4efa6a57eafee95cdf36131896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 23:14:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 Jan 2026 23:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:15:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:15:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:15:05 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:15:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 Jan 2026 23:15:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:17:57 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:17:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:17:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:17:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:17:57 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 23:31:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:31:20 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:31:21 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:31:22 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:31:22 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:31:22 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:31:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:22 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe374cc1a9b8c53473ffdcc716cd879254a8b068db2dd4c78b47e812bd5002e`  
		Last Modified: Fri, 16 Jan 2026 23:18:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5639f313e2e1050528e357b95c31114f84f32e9a9efc5fb02b87c3e108474d39`  
		Last Modified: Fri, 16 Jan 2026 23:18:19 GMT  
		Size: 116.1 MB (116138771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b745b2bfec8c8d86d18897851c9e3dbee03592d1b706a5f28ad5797d7dadeb`  
		Last Modified: Fri, 16 Jan 2026 23:18:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d4c037abdcfdbc491dc2280b0ae5900abe60d7f0fbe9550b61b8a76ec4e6ac`  
		Last Modified: Fri, 16 Jan 2026 23:18:27 GMT  
		Size: 13.8 MB (13816856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbe9a54efdb9108146da87246d0f6cef60fc285c477ad11f8006d8b9f9c38c2`  
		Last Modified: Fri, 16 Jan 2026 23:31:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73fee9220efc80cea13016a3df405e0643e056ea06b3c6fbca5bd29f7f97b82`  
		Last Modified: Fri, 16 Jan 2026 23:18:18 GMT  
		Size: 14.0 MB (13968105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf2e68da889959ae0d92ccad3b7cfcf84dbd37dcdb0f7b287dcea9d4cc310cb`  
		Last Modified: Fri, 16 Jan 2026 23:18:18 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19cfeecbd3ed1fef4c299d835ec05c463a1c3f04ad39e4b06cc116793fbbb3`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200a6586b4d9b61b743ffe2d1268ec022cd023b06c45bd9e42d697ea1bcef0d7`  
		Last Modified: Fri, 16 Jan 2026 23:31:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77dbcae43d9b3f07b882cb01173256293a62d92c1cd2bcd3aa28752697657c9`  
		Last Modified: Fri, 16 Jan 2026 23:18:20 GMT  
		Size: 9.3 KB (9271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54914f6bac8d9a6b118957f54f307c5a7ddb031f54ed57cd88ddbad805075752`  
		Last Modified: Fri, 16 Jan 2026 23:31:47 GMT  
		Size: 26.9 MB (26872018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8412b26869b78f61c61053ee5ca9353aed52899027a26d882adc6dbca898f40e`  
		Last Modified: Fri, 16 Jan 2026 23:31:51 GMT  
		Size: 31.8 MB (31847669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368b19bd2d7cd6663581a5524a2162bc736dbec78614be4d94c868a42cd402e`  
		Last Modified: Fri, 16 Jan 2026 23:31:43 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6623d9e1a7116037d9b4021c2b5b396c799dba8a979ca0bab4645ce91c438b`  
		Last Modified: Fri, 16 Jan 2026 23:31:43 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006553e9e0dce1b3892829fcd27723257e5b2b36f74782faea6077627534b56`  
		Last Modified: Fri, 16 Jan 2026 23:31:37 GMT  
		Size: 27.0 MB (27024654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c442dad169a60c58868f36ec422edbaeef83e0d73c18a0dcdbeac60a5cf46ea8`  
		Last Modified: Fri, 16 Jan 2026 23:31:36 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f567ab2e584e50125a556203006a7e10e3c1a9a9c385b009fc664ecb375f53a`  
		Last Modified: Fri, 16 Jan 2026 23:31:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a84831deca1ac7923ab7d153c906973e6103df90cc783ac95c25bbff021f77`  
		Last Modified: Fri, 16 Jan 2026 23:31:43 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:f7a3eda52d750efbe8fe1af793065ab4298751d8ccbe1812c61f733fb74d8f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f8619f8f07fab8a782a67aec39e26a5b8c484e7709b475deeff20ae71633dc`

```dockerfile
```

-	Layers:
	-	`sha256:1a0cd26c137bb6f251347775ce026e470ca3a07cfd8440f6a622d0bcc47eda9e`  
		Last Modified: Sat, 17 Jan 2026 02:15:31 GMT  
		Size: 8.1 MB (8121563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d208802848dd55a74b07af91ed79dab856f8a4c7a4beaac2dfe137870dca30d7`  
		Last Modified: Sat, 17 Jan 2026 02:15:32 GMT  
		Size: 52.0 KB (51958 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:1e4f353376959b91839a4f77255c88c901bff80103b4a2187190cb75e58a1840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258294206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63734cad05af74de7bb4be76a6b4179a470794b3aca55b9fb4e9895a45d670e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:49:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:50:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:50:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:50:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_VERSION=8.4.17
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:51:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 15 Jan 2026 23:51:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:00:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 00:00:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:00:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 00:00:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 00:00:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 00:00:55 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 00:03:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 Jan 2026 00:03:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 Jan 2026 00:03:28 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 Jan 2026 00:03:28 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 02:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 02:58:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 17 Jan 2026 02:58:50 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 17 Jan 2026 02:58:51 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 17 Jan 2026 02:58:55 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 17 Jan 2026 02:58:57 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 02:58:57 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 17 Jan 2026 02:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 02:58:58 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 17 Jan 2026 02:58:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Jan 2026 02:58:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729c2d5c144b66bc0a7de79ce37a807764c298349e33d3b4d2b9ffc6e4f86da`  
		Last Modified: Tue, 13 Jan 2026 01:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5312002cd976a0822f64d1b71b8a785c0ab1242111634934907ad0ff8cd084`  
		Last Modified: Tue, 13 Jan 2026 01:56:07 GMT  
		Size: 109.6 MB (109597601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c320c737217d4d4f5283740cc3e07729118082922eab5fedf369acbd762089c`  
		Last Modified: Tue, 13 Jan 2026 01:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb77a75fd239e13e4fbc113878833f5eeb5d00571dd6b1fe3385beba4e00bb5b`  
		Last Modified: Thu, 15 Jan 2026 23:56:53 GMT  
		Size: 13.8 MB (13832266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4edb8b3202ddfe32403db809adbb32d945196145e043d12d5a58365a28281d`  
		Last Modified: Thu, 15 Jan 2026 23:56:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e81c6863f307b59f791e6db19cefffa3a35e06f120a7debc4682841b17e7d9c`  
		Last Modified: Fri, 16 Jan 2026 03:26:35 GMT  
		Size: 14.2 MB (14211973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce3d0921113c53f5aff0fc5c39a25e46b683b795e5bd6f942fbda76374f13c`  
		Last Modified: Fri, 16 Jan 2026 00:01:27 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2990feac47ed10e958f904d1c8a6006e1e2d4040c96c01dcf9280517490ff4b`  
		Last Modified: Fri, 16 Jan 2026 00:01:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ea150dbccc439ddbaefab4e1023210bf2f2600f0e8d29e40c7d1d31c0dfbf`  
		Last Modified: Fri, 16 Jan 2026 00:01:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afa7115bfc6b84d5fda358af6cdabf8bf3f51f4a9be38879bd46ec47904bffa`  
		Last Modified: Sat, 17 Jan 2026 00:03:59 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7a463ecd99a0d23356a6dd9ca799fb9542c2acc2ad231bbc191b29db70979`  
		Last Modified: Sat, 17 Jan 2026 02:59:48 GMT  
		Size: 27.5 MB (27504476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6be4eb4d853ebd85d9e598ce105fe8322cae5e88fd8112227f7e50c730e274`  
		Last Modified: Sat, 17 Jan 2026 02:59:57 GMT  
		Size: 32.5 MB (32509283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1604743717bbaa9717f431a07716a43adfa7ec4c6e319a71bb3b5760bf23497`  
		Last Modified: Sat, 17 Jan 2026 04:35:31 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d5c6b2dc075dcde18dc65c0ba3990ed086dd068d33bb9f5426318c0c183326`  
		Last Modified: Sat, 17 Jan 2026 02:59:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e59d55b6486f266cf5cc2cd947f5fbc996703b786cf96d79a70773405941a7`  
		Last Modified: Sat, 17 Jan 2026 02:59:57 GMT  
		Size: 27.0 MB (27024681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4642323ae7890183d5357c2ec439b33ea8d994e614afb4353bb1355ebb93b148`  
		Last Modified: Sat, 17 Jan 2026 02:59:48 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7502c686c073d9a1e940731c6b58972e28372de8185943085fce79593356d038`  
		Last Modified: Sat, 17 Jan 2026 02:59:55 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e0bfe94c3ac1897f6d583c414f191365812b928ce7c6bbdb745bd93ce4e71a`  
		Last Modified: Sat, 17 Jan 2026 02:59:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:d8d43d31feba9e81ac66793b255890897a6739120feefe64d16b352de41bd3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8201268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea2e6ae007c093913b704cbc74fa16eccc0f3471d50fc571673d209ba5d6ad`

```dockerfile
```

-	Layers:
	-	`sha256:e1c884dabb62ec77e0d768d090c6e71df0a2f7c2684be9b4e1189f4caf269cfa`  
		Last Modified: Sat, 17 Jan 2026 05:13:41 GMT  
		Size: 8.1 MB (8149214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4ead538fd92dbe3927daf581015af31081bcbb66f3d81e5f3c551b80e8bf4f`  
		Last Modified: Sat, 17 Jan 2026 05:13:42 GMT  
		Size: 52.1 KB (52054 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; riscv64

```console
$ docker pull wordpress@sha256:478b7cde31d661f5cbe3dc6587b0337aa8a0742faf61f67d48edb7ce7f9d172b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284506800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ed6a8dfbfdd10f5ec0709aed3f37d3a938839bec1aa2a672fae615baefcf07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 16:40:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 14 Jan 2026 16:42:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 14 Jan 2026 16:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 14 Jan 2026 16:42:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jan 2026 16:42:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jan 2026 16:42:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_VERSION=8.4.17
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Wed, 14 Jan 2026 16:42:01 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Sun, 18 Jan 2026 00:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 18 Jan 2026 00:52:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 03:42:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 18 Jan 2026 03:42:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 03:42:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 18 Jan 2026 03:42:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 18 Jan 2026 03:42:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 18 Jan 2026 03:42:23 GMT
WORKDIR /var/www/html
# Sun, 18 Jan 2026 03:42:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 18 Jan 2026 03:42:23 GMT
STOPSIGNAL SIGQUIT
# Sun, 18 Jan 2026 03:42:23 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 18 Jan 2026 03:42:23 GMT
CMD ["php-fpm"]
# Mon, 19 Jan 2026 14:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 14:36:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 19 Jan 2026 14:36:15 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 19 Jan 2026 14:36:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 19 Jan 2026 14:36:24 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 19 Jan 2026 14:36:24 GMT
VOLUME [/var/www/html]
# Mon, 19 Jan 2026 14:36:24 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 19 Jan 2026 14:36:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Jan 2026 14:36:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 19 Jan 2026 14:36:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Jan 2026 14:36:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5316a37adfe759942e176fd7f10a29d05b3a11f1e1ee941f4e57475f602a088b`  
		Last Modified: Wed, 14 Jan 2026 17:46:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4446eab7b758c11057a2a24af5250e361ee957c8bbeefbbfe2d0589362c88b78`  
		Last Modified: Wed, 14 Jan 2026 17:45:59 GMT  
		Size: 146.6 MB (146578411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab7a0d39d3c969a3d5797534890fb011b1e36b12815336c2b2920d0b178acf`  
		Last Modified: Wed, 14 Jan 2026 17:46:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ab7bd0ed6714195572d20f7ef625e9b492fd95c55a8bd8bfdeb6e593653b0`  
		Last Modified: Sun, 18 Jan 2026 04:18:15 GMT  
		Size: 13.8 MB (13831950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b9f34a5cd58e73fae110fc104e4f0fc2eb992aeba3be36791d5381e2ec89ad`  
		Last Modified: Sun, 18 Jan 2026 01:50:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0458b1a0c84e0d52afb2ddb96fc8e4ec318a747e30f8f4beee1cff9d65269aa8`  
		Last Modified: Sun, 18 Jan 2026 03:45:30 GMT  
		Size: 13.1 MB (13136952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827e0b83cd73aae6d0eea78b38360a51b79206dfd823fd0740e3b5fe7bfac452`  
		Last Modified: Sun, 18 Jan 2026 03:45:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9bff690761e087b769178fc99016a722f14a2b33bb10d39e432612ad7fef7c`  
		Last Modified: Sun, 18 Jan 2026 03:45:18 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5a8cba7070eb17ad4a666f522e07ebac16d61a8f13ae55c817925235637773`  
		Last Modified: Sun, 18 Jan 2026 03:45:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a1ade0406ae3c00043fcc384bda443d00aedbf3be67ea77847bcda5872eb3`  
		Last Modified: Sun, 18 Jan 2026 03:45:28 GMT  
		Size: 9.3 KB (9274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0139f7134aa9d67068cf0f30d9360696f9e14795eaea6f704e3305a7a3f939`  
		Last Modified: Mon, 19 Jan 2026 14:40:46 GMT  
		Size: 26.3 MB (26252219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c98f9101a0cb0ddf13fe3cab3e275a32930a23c4cf8faf60d11a7b06a5ca876`  
		Last Modified: Mon, 19 Jan 2026 14:40:47 GMT  
		Size: 29.4 MB (29392581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37397892656d5fce3ecb0013912534f4d54f411ea7a24ea7226575f0045f99e`  
		Last Modified: Mon, 19 Jan 2026 14:40:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cef5a53f0e1b42ad7e1b5b2007580d34f23350c9664feb25b2348b005c64c2`  
		Last Modified: Mon, 19 Jan 2026 14:40:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f416a806ff09f3064504ba76b2e6fd09543399b2ae8c23ac25debec8bb9081`  
		Last Modified: Mon, 19 Jan 2026 14:41:17 GMT  
		Size: 27.0 MB (27024683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8af20dfb89e2dac729d566b7991979661ce456ce7226e40cf4dfc8f5cfc2d`  
		Last Modified: Mon, 19 Jan 2026 14:40:38 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b5c4c90fcc50afb42a1f54c0157408bb3149a3b3ab976bba60bc2f14d71a37`  
		Last Modified: Mon, 19 Jan 2026 14:41:14 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d0a2fb659ec01255502c3da6be9bf7aa98e54a4844dad661926533a24852a`  
		Last Modified: Mon, 19 Jan 2026 14:41:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:89df86a77d171595ad96ec6bb2c9f5c1b9d011e720ab993877f93d5580d9b652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8271689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4be134a4bd4dca914106c9646857dc1d1a0e63e9f060dd3827f8a454308c10`

```dockerfile
```

-	Layers:
	-	`sha256:80191ba8523d79371a7db633269c707387c1b8bac10d27724eb711f8ad0d3378`  
		Last Modified: Mon, 19 Jan 2026 17:13:35 GMT  
		Size: 8.2 MB (8219635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b76ad1e7c7610a6eca599a232c72e70a48a6d3de4c3848e63fa29dfd7c2b75`  
		Last Modified: Mon, 19 Jan 2026 14:40:35 GMT  
		Size: 52.1 KB (52054 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:af67865c2c2c2ea30e0ab07087c5e09d8f7076965157977624ec3e4b3fd800ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233674301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da12fa0875b4e3382fcc56ea00e03eb00d0c6e58db4a18ce7d3fae2460939d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:17:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 14:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 14:17:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 14:17:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_VERSION=8.4.17
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Tue, 13 Jan 2026 14:17:46 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:29:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 15 Jan 2026 22:29:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:33:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:33:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:33:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:33:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:33:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:33:20 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:32:03 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:32:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:32:03 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:32:03 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:58:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jan 2026 00:00:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 17 Jan 2026 00:00:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 17 Jan 2026 00:00:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 17 Jan 2026 00:00:17 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 17 Jan 2026 00:00:18 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:00:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 17 Jan 2026 00:00:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:00:18 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 17 Jan 2026 00:00:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Jan 2026 00:00:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c4733797eaec0989a1cb932b369157d931d307832b702e0c607591b7544acb`  
		Last Modified: Tue, 13 Jan 2026 14:22:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea5b2cc903169cc341ae9e639a95aa0c1455c7ac2978fbf73ee1237e37e617d`  
		Last Modified: Tue, 13 Jan 2026 14:22:24 GMT  
		Size: 92.6 MB (92565718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206fb82eaea09596a170661373ee71e071302bff3ef17280c322638e50bddc45`  
		Last Modified: Tue, 13 Jan 2026 14:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11971a1f64208d36864cf4271914aaee30e90a4be19de23a719a0570fefefdd`  
		Last Modified: Thu, 15 Jan 2026 22:33:50 GMT  
		Size: 13.8 MB (13831322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6eb7677733b51ed3ad64c6283a1ce65f0b816d3d9e0acc29eb472c261f5346`  
		Last Modified: Thu, 15 Jan 2026 22:33:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665ce36f5c6b2cfc002115e7a5b0290e4bbbd25277bcc02690c2f57ba253e2e`  
		Last Modified: Thu, 15 Jan 2026 22:33:54 GMT  
		Size: 13.5 MB (13461332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2747a3a0aaea81da4ff434198ca692c46ce1ee7fb61c8f2e96e7602220513`  
		Last Modified: Thu, 15 Jan 2026 22:33:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f0f305b59b3be21bd1ccb2ca37977dde176e76e698b47b4d09965b581fb5d1`  
		Last Modified: Thu, 15 Jan 2026 22:33:49 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af99b03df853cd7f9b8c735ffff3c34ea3cb8e669ef398224f2c10ef8517e97`  
		Last Modified: Thu, 15 Jan 2026 22:33:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457f8064aec98aaec3ee4fcc91a69e42d963d8f3c034712d067558e44e102aa`  
		Last Modified: Fri, 16 Jan 2026 23:32:22 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718473a5e3f6f72935983bdd16a357e6469c37e65a143b8b3847f48319d2412a`  
		Last Modified: Sat, 17 Jan 2026 00:00:41 GMT  
		Size: 26.6 MB (26605857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8ce468d69477a23af908bd4b0fb4b2acda42da1d84cdbd3bcdba46513df358`  
		Last Modified: Sat, 17 Jan 2026 00:01:03 GMT  
		Size: 30.3 MB (30333688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ba03f5e7f89768ac2b234043560b84ebdb9e072c624437b5e06131e3bad57`  
		Last Modified: Sat, 17 Jan 2026 00:00:58 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b098b29c84e5a7cdaff89cc6b4c0744d4c053c2dd6c73dcbfee9ffe60ae9d7`  
		Last Modified: Sat, 17 Jan 2026 00:00:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094bcfa3b522ed89183d38d4ab8e70648e3cb14d23f277badf612564d53e6dd`  
		Last Modified: Sat, 17 Jan 2026 00:00:43 GMT  
		Size: 27.0 MB (27024657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47063b35d3d809a98b52207ee1e6e869eb312a244b42c3471faf20051a63b8b`  
		Last Modified: Sat, 17 Jan 2026 00:00:58 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b68c0b1d76501cf0d2a27eaee289f65ec02ed3399fbcde59d61b82b3c6331d`  
		Last Modified: Sat, 17 Jan 2026 00:00:58 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1577b7e76cc1ce570dce58df51ecf569bb87c86af2c2504afed342cad74ce50`  
		Last Modified: Sat, 17 Jan 2026 00:00:44 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:0fe19a9e5ff6b4e8228f90b857ccfe10c8532ae895c3b12fd47e322bc86be503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e81559566baac82a11441981cc6b1959f972bc1e3551055b14a560602e0778`

```dockerfile
```

-	Layers:
	-	`sha256:cf19dcd205c38d44da7e05b7098ff1442734bec378cf8bf25d4fb4f13e9c35de`  
		Last Modified: Sat, 17 Jan 2026 02:15:52 GMT  
		Size: 7.9 MB (7873131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b7270ed21b05e7d0b31f2c9d87a4f126d34f516f255aee9ad39ec4a5e5c90b`  
		Last Modified: Sat, 17 Jan 2026 00:00:40 GMT  
		Size: 52.0 KB (51990 bytes)  
		MIME: application/vnd.in-toto+json
