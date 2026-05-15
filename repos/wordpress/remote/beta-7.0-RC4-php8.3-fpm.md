## `wordpress:beta-7.0-RC4-php8.3-fpm`

```console
$ docker pull wordpress@sha256:09eedb4c140411f49343c868b0663f3b83567bfd17d9f762e41c67000969e14e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:a3ffafd181e4a55a3e7b9a3a2ad28e341be7f1c5cd4b465f62702f0e4ecdc2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264932808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af58da9bc97d253ba1bd386a4ed275b252c01ec52fa88c6ece63f6d89ba897a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:23:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:23:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:23:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:23:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:23:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:23:41 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:27:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:27:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:29:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:29:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:29:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:29:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:29:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:29:34 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:29:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:29:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:29:34 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:29:34 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:57:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:58:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:58:59 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:59:00 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:59:01 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:59:01 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:59:01 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:59:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:59:01 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:59:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:59:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f9f996dc712eec9875e95aee9a82a598c21224a57c9c80c2565f7d0440a945`  
		Last Modified: Fri, 08 May 2026 19:26:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5d15ef7c748f655723578247dd8046b74d79552f9b14cba5afa2a1daf1641`  
		Last Modified: Fri, 08 May 2026 19:26:51 GMT  
		Size: 117.8 MB (117842213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488166dcddd315533e51a5270ad5cfbcdac9e6a4f0eb2763a6ca6fd9965cc293`  
		Last Modified: Fri, 08 May 2026 19:26:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba155a624e60d29b3a199d4f808629784da680914c47db471b85a5f3b414d633`  
		Last Modified: Fri, 08 May 2026 19:29:45 GMT  
		Size: 12.8 MB (12751411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdc597721891712910f0a29dcd8769055a12a52e10b5792250e4cb739c8b58c`  
		Last Modified: Fri, 08 May 2026 19:29:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16225ad2d1646ae2f8d3029dbe1bb4998e8b5d0ad8e072eb5b2dbab1d650e57b`  
		Last Modified: Fri, 08 May 2026 19:29:44 GMT  
		Size: 11.9 MB (11902297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf55a0cbd4129370c3bf8039ab4977391740ed0ddebd53cdcc091545c7a7f57`  
		Last Modified: Fri, 08 May 2026 19:29:44 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d58c8e2880ae9049162980fc91250b5c737270d31b638409230f99b5ed1e4a`  
		Last Modified: Fri, 08 May 2026 19:29:45 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329e84d837c87a6a4c965e95b9ca38701612a2bb947f2a0cbc8e248fbcc4e8f3`  
		Last Modified: Fri, 08 May 2026 19:29:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc9758089bfd4e7082e87863de8c160e1beac2a4dc73645cc4267ffa5a85c52`  
		Last Modified: Fri, 08 May 2026 19:29:46 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e98ac0fd9f786fe25f257b21b5934fc58884beb3d5faa4179055887ebefe273`  
		Last Modified: Thu, 14 May 2026 23:59:19 GMT  
		Size: 33.1 MB (33076803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdac86dd00e3701ce4fa36353d5801b0f1c51d3dc6628ece702acc278b9c4d10`  
		Last Modified: Thu, 14 May 2026 23:59:19 GMT  
		Size: 29.9 MB (29913538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bb5d7fd383ba843b60d0d69e6d100eadb519925ee81745d51afe462f432f21`  
		Last Modified: Thu, 14 May 2026 23:59:18 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e02bead3f8d5ee2fc832d6e140684c01263597d290337bde9be563542bf51`  
		Last Modified: Thu, 14 May 2026 23:59:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385af7126d7cdcaacb65a3f3c6ae78d68c001bed7dc38b8521ef94f0b5610bd9`  
		Last Modified: Thu, 14 May 2026 23:59:20 GMT  
		Size: 29.6 MB (29648015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b55950cf95f47a569976562835ce99d2631d0fe109361c1ac1a74113b9161`  
		Last Modified: Thu, 14 May 2026 23:59:19 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d01f429c7855439853a766ec1737b8ffb848475f77faaca545d28dd716691d`  
		Last Modified: Thu, 14 May 2026 23:59:20 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfb826a066f631a0d17dc404eb0e24431d58c5002912c80fa0867487bc576cb`  
		Last Modified: Thu, 14 May 2026 23:59:20 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:10e8174caa5887649cd09e793c5b7a0ab4d2c6aa6ffa48afa9e68068deba7815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8225407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254147f7c8c146473ca237523df450008af0c6ec997a6722d01e34e00f909ab2`

```dockerfile
```

-	Layers:
	-	`sha256:5a6910e030a58d7c53c9173750ae93643029f6da8d89c1e428e41088dec2c74c`  
		Last Modified: Thu, 14 May 2026 23:59:18 GMT  
		Size: 8.2 MB (8171659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f864c5025f1c1bc5a02e0993e6dd415f376649b3c278bb67739f26289aa62a3`  
		Last Modified: Thu, 14 May 2026 23:59:17 GMT  
		Size: 53.7 KB (53748 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:e452977c40f8e41407f6b876196b487b629b742219a838f37390398cdf9fc20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233480659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9820662efc85633507aeffaa53807f3224ee618b3808ffa3dc8ff2a769908d53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:26:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:27:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:27:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:27:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:27:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 20:27:15 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 20:35:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 20:35:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:37:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:37:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:37:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 20:37:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:37:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:37:49 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:37:49 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 20:37:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:37:49 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 20:37:49 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:56:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:56:47 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:56:47 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:56:49 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:56:49 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:56:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:56:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:56:50 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:56:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:56:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0c566908ea539c3e25f1285e63b6797ddded9bb42d084d9f81f4b7c019049`  
		Last Modified: Fri, 08 May 2026 20:31:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022376530e342f2b307a2b76a1b2782ac9bd5f3ac062c72e4ec7eb11ee308b6d`  
		Last Modified: Fri, 08 May 2026 20:31:06 GMT  
		Size: 94.9 MB (94884438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736fe276f2af3aa4c4f3f3a7f37065685be7205241ac76c47a9f7753e4431f9b`  
		Last Modified: Fri, 08 May 2026 20:31:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c68c7fe390ab023ec97dc61b1d467a97af63d49af4e33701bb55f8db339ecd`  
		Last Modified: Fri, 08 May 2026 20:37:59 GMT  
		Size: 12.7 MB (12748913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfc897c986b88110d69555305dd2ab712f55f40f317b4ea8ee147891b6cac52`  
		Last Modified: Fri, 08 May 2026 20:37:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51e95a85bd6abe694808d92b949bc9f17bc8548a4a6dc46057820bc0a7d61af`  
		Last Modified: Fri, 08 May 2026 20:37:59 GMT  
		Size: 10.7 MB (10694856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ea54100ab535b4bc27d0911f098f780989d80df5a666aca04399c40ebf867a`  
		Last Modified: Fri, 08 May 2026 20:37:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ed03785104ce6d6808111d9240b6911d412990b8d1c7eefeb74085ce9423a`  
		Last Modified: Fri, 08 May 2026 20:38:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17eb5d9d3134415dc04de46d4725475a445acf4a398557044876075fbb2de2`  
		Last Modified: Fri, 08 May 2026 20:38:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f1bdc2c2884dfa005a209846f5efb239b7364d997a7022eabb279beef351a7`  
		Last Modified: Fri, 08 May 2026 20:38:01 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21531d94b2452ffcf740d000b83822fe5e41a3a80f1ded49c343d6d36d8c5546`  
		Last Modified: Thu, 14 May 2026 23:57:06 GMT  
		Size: 30.3 MB (30252871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a248f5272471bdc373e154b1a1aa49fe2b35f9d81b24e7310c808ac383ee38`  
		Last Modified: Thu, 14 May 2026 23:57:06 GMT  
		Size: 27.3 MB (27285055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50568486328ff569d5b4110c6edc52f986aa0763182c62c831a6ee5b266e356`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96328aef5db681bfad821af0f1deec71609bad485c1514d148482b23c6e28aa`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572c00766abaefa9693578027a20ecaa89947f859285c3b23f064aaa1969e14`  
		Last Modified: Thu, 14 May 2026 23:57:07 GMT  
		Size: 29.6 MB (29648024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ad41cea8774acccd6aef88c2dcaba0912ccdc8a3d529adb3bdcfad95f4af4`  
		Last Modified: Thu, 14 May 2026 23:57:06 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f4461aaf097ca54ba9a1360768aff6ee2de319616039937779e9cf3e9d737f`  
		Last Modified: Thu, 14 May 2026 23:57:07 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fd0d0d6c7794ca442187a78f48af0e4fe9f36371c4d14da5e1e8001861f982`  
		Last Modified: Thu, 14 May 2026 23:57:08 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:1f96b5bc0a9669260e19b382a1d88163defec78764ed8387b06dfe7e1fbe239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8019120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1165c35f4ec27491323b574c49dc8ce7752a30229e80fd8bb7fe982447c6fac`

```dockerfile
```

-	Layers:
	-	`sha256:e04f08c01290596a02c623f2bc902e04481f2404731d53079308c1561ee06680`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 8.0 MB (7965204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87951427a84b8cb7743ab0129761462ff2f1c888e3801332e23be7662c695ec9`  
		Last Modified: Thu, 14 May 2026 23:57:04 GMT  
		Size: 53.9 KB (53916 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:16b1f26d36d407fadde09b910bb46f13ebb77e6f951521bf046801de500b60c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219822068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3f166c54ef2fcb6aa025838926ef048211f9c5aa896c81740100150366d687`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:16:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:16:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:16:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:16:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:16:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:23:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:26:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:26:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:26:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:26:17 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:26:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:26:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:26:18 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:26:18 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:55:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:57:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:57:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:57:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:57:27 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:57:27 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:57:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:57:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:57:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:57:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:57:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f802c17af1af5c81f3e9b807af5c1106bf2eccef0ea2ace097ee66e9daea5b6b`  
		Last Modified: Fri, 08 May 2026 19:20:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721671956530437d5200ca7c1d9408806fdffe5cab95634848f1fecf6a8e20c`  
		Last Modified: Fri, 08 May 2026 19:20:04 GMT  
		Size: 86.2 MB (86249709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfdb6e3ae44c13caa77a3fc583916405db6dc3d5e409a460dd1535f5e18ca2e`  
		Last Modified: Fri, 08 May 2026 19:20:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58d26311eed50f778076fa95f0892a4da31b84060a199525746ae659176eb70`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 12.7 MB (12749031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f952765c689d17da7b9ab36002e95a5f7f3e6537542a3ee4b6d401e75e16f4`  
		Last Modified: Fri, 08 May 2026 19:26:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45365650e9501f1756a902b0b04ae37888319d72e1f84155683a9bad4e63fcdb`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 10.1 MB (10086242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126da415fc5d9c32cd167cce894f4da83b8c83e5402f53cff2794a2275d6922e`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc944f7ccf5a56e4ac254ea79968ad6ef32d2ffda9ac50c395737c4b98e52603`  
		Last Modified: Fri, 08 May 2026 19:26:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6b92abde2fce6f9a961165f122418b6b2344880368b2b3d7c48f33589e32c`  
		Last Modified: Fri, 08 May 2026 19:26:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6087bf797ce1bbf009e1e8ff8e2b88bb4ad86ad12e7829284fb3ce5dbe07679f`  
		Last Modified: Fri, 08 May 2026 19:26:30 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7f60c1d8711b7ea314f16577090905e372455325a2be300bf020d7b6432329`  
		Last Modified: Thu, 14 May 2026 23:57:43 GMT  
		Size: 29.1 MB (29132993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2dfde7bb955a1b992ded97036b5b0c85960992a0fb6d91f5c44e5cb18ba0c`  
		Last Modified: Thu, 14 May 2026 23:57:43 GMT  
		Size: 25.7 MB (25722859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0a81d7a86aec158b9df25305fd87497506b9fa7dfab3aba5c55141abf753a`  
		Last Modified: Thu, 14 May 2026 23:57:41 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8d29f921b20fc3c006bc4a61c957061bed379f7b66cd84376f75ffeedf3a4`  
		Last Modified: Thu, 14 May 2026 23:57:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e113ffce4a13791d83e5a1bbb0108509b07879574594da18e2cfd20d5eac2a`  
		Last Modified: Thu, 14 May 2026 23:57:43 GMT  
		Size: 29.6 MB (29648014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0dad464e979b685d7b7f2c57d824a61a82929516bc5a07f372de71ed832f3`  
		Last Modified: Thu, 14 May 2026 23:57:42 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5016427c53b22fe4df9f6f0520a58a3704cd380779d857128a2c37734f12c31`  
		Last Modified: Thu, 14 May 2026 23:57:44 GMT  
		Size: 1.8 KB (1774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56825049f2b785f19c29fc0cdece0a102624fd752431824120391dc89c8fe392`  
		Last Modified: Thu, 14 May 2026 23:57:44 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:ad408a99b09dfb5d95c8dba35bec7944aaae8a1b425f58a2a38da4b6aaae3b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8023926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc55ecdd7775c24a5e5a8edbbf5c99c1ed2419e1184e1869c9ea19791ce0ba5d`

```dockerfile
```

-	Layers:
	-	`sha256:05d5b7f22e4fb44ef75f08f2ff8be5433d6e1ffce05e89a739afbd97d9ffa635`  
		Last Modified: Thu, 14 May 2026 23:57:42 GMT  
		Size: 8.0 MB (7970010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21acec71f58d9cd63090d771397cfa6e3714bbbcc1b3d93825ee77d5f70cb80d`  
		Last Modified: Thu, 14 May 2026 23:57:41 GMT  
		Size: 53.9 KB (53916 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:e06ede457e49d02c11da46ad79ede7d0089eb910d2391c4ef44a396ca75e8f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257475194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2117e3d6477d72ca9fdce62759f5f8c7e62cb0d4ab9672ce4ce9d11e818290fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:23:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:23:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:23:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:23:00 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:26:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:26:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:30:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:30:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:30:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:30:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:30:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:30:22 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:30:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:30:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:30:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:30:23 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:55:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:55:18 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:55:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:55:20 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:55:20 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:55:20 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:55:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:55:20 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:55:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:55:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8086bfd6505019c7c45ec04b34146fbd2b5c804a3a48f0090d06f398bed6cd5`  
		Last Modified: Fri, 08 May 2026 19:26:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5bd2d7f718b994746e21b85be840dcb74b8cfcfec7b57d024701fa91da09f`  
		Last Modified: Fri, 08 May 2026 19:26:26 GMT  
		Size: 110.2 MB (110165326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d15e587523109351fba67dac8f446e6a94b4e13d99b55081885e900fcdbbc2`  
		Last Modified: Fri, 08 May 2026 19:26:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efbf55f3c7e296bc13cd61f6ecb4e63e74b72ad5d603a3e2b2fbe7b3ea1a1a7`  
		Last Modified: Fri, 08 May 2026 19:30:34 GMT  
		Size: 12.8 MB (12750956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dd7b0b7787802f91cc154e69dd460fbe120c3595c09b2c19c9f69758c84921`  
		Last Modified: Fri, 08 May 2026 19:30:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e380c31995e19f95a6d952d526f4ff5e1bbe162decdce940b32c5b5742167629`  
		Last Modified: Fri, 08 May 2026 19:30:34 GMT  
		Size: 11.9 MB (11925447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf334d330dd3b3e633744a3bee1a87a4c0742196f361a7200a3d8ba54e7e352b`  
		Last Modified: Fri, 08 May 2026 19:30:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24edd16da2fb68fddece29989dc7cc76c5fdcd813c0edcb8208469f2ef31be52`  
		Last Modified: Fri, 08 May 2026 19:30:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d94a1fc2d51a0530677cf03e9bc8278c2c458818d4fd92dcc091aff48b56e`  
		Last Modified: Fri, 08 May 2026 19:30:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee679c4f3b497f600e5893357d25b0fd4e09c8adf76d868fc0c3c1ed61bc3e6`  
		Last Modified: Fri, 08 May 2026 19:30:35 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55099939fbba19a7ca035b39823a66651fa92706319b0795cb2fe74b369a9065`  
		Last Modified: Thu, 14 May 2026 23:55:38 GMT  
		Size: 34.6 MB (34580237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de78f0373e2dd126d641ef10a3f71be1427849aab4be192277a39ae3605dda2`  
		Last Modified: Thu, 14 May 2026 23:55:37 GMT  
		Size: 28.2 MB (28243280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf371c4689a4e8ea5077ee030177ba0cd7cf0d630dbd0c0fcddc83361ccc666b`  
		Last Modified: Thu, 14 May 2026 23:55:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc42bf893bca0f0979ba786b17a3c1a0db3fb5628eb347f458230e9ad4e89246`  
		Last Modified: Thu, 14 May 2026 23:55:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59853bec87526bcadf064adfdba112c5b686b3e49febab311b0a873740ed61a`  
		Last Modified: Thu, 14 May 2026 23:55:38 GMT  
		Size: 29.6 MB (29648015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78382ab18a8298bc87cd720299b3f04e69a9378c45c2fce8503833cd9496b07`  
		Last Modified: Thu, 14 May 2026 23:55:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e32a91185502db5cdccaca176414ae5f2b9296513c6e89edb374ce566fcffa`  
		Last Modified: Thu, 14 May 2026 23:55:38 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d30a2d21653e752a3bfc27cc0fecb9ac0988f95eadef3f43c7ba27233072c7`  
		Last Modified: Thu, 14 May 2026 23:55:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:25ce0f10772c9d1fbe193c8a728065dfef760b2e732e2897dacb506d35b9fb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8322138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f373f63e95441a7fa79d42e34a1300914fd043c7a38f8454e81dce32df0b83`

```dockerfile
```

-	Layers:
	-	`sha256:80a115956129f32dc17dd09de248756e9ea1faa73c4fd08f4de1e9862027f8f8`  
		Last Modified: Thu, 14 May 2026 23:55:36 GMT  
		Size: 8.3 MB (8268163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b28de5fb0070738ab3ad708e6fa16505898fdffcf8da85b2077bff758c8d77`  
		Last Modified: Thu, 14 May 2026 23:55:36 GMT  
		Size: 54.0 KB (53975 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:3c7b9dc0b568ea123764ce39ddbf737bf2759353e6de242627cef6c9c29d08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262478133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273108c352532ed884c9d9510e58cea2871d41d563f28aa5d475747f4148a730`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:21:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:21:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:21:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:21:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:21:52 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:25:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:25:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:28:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:28:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:28:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:28:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:28:01 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:28:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:28:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:28:02 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:28:02 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:55:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:56:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:56:46 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:56:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:56:48 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:56:48 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:56:48 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:56:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:56:48 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:56:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:56:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d6f3c83c74c654dd6246149e49404a2e69c4ce6834bcc08fc80d8b4cb66c08`  
		Last Modified: Fri, 08 May 2026 19:25:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6c0962594c8389dc87b4b94336c90411bd79346ea9b68a2ce52db2dd85bb58`  
		Last Modified: Fri, 08 May 2026 19:25:10 GMT  
		Size: 116.1 MB (116144409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c9ce494d7f7363ad8ccbad4905c51490694c7694d1aa86e40ee6d9b1f4835d`  
		Last Modified: Fri, 08 May 2026 19:25:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e6d0070ddefc823f7d52c2e85aa95aaf83e1e066325b660949bd15ee13870e`  
		Last Modified: Fri, 08 May 2026 19:28:12 GMT  
		Size: 12.8 MB (12750287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1f31a64e4086bddb3d6899dafc72d55831060d92a0327c365b48da41fd38b7`  
		Last Modified: Fri, 08 May 2026 19:28:11 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0cb158d63418e29e01208091b5f820399a185fe0abdef2b4e22ad2700009cf`  
		Last Modified: Fri, 08 May 2026 19:28:12 GMT  
		Size: 12.1 MB (12109738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec3e5b88dab107776f4702a7e6323cce896b7a038f01d993a8aa27231692273`  
		Last Modified: Fri, 08 May 2026 19:28:11 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02f2678a2698a3ba11ce4efed422273ed7453a444640605200de5eb5d65a6a9`  
		Last Modified: Fri, 08 May 2026 19:28:12 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2448bf7782615043bec47daa850049755276bb3519479fe60af9fccbb3e516`  
		Last Modified: Fri, 08 May 2026 19:28:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce2bfca9a456b1834a7cb5344f30163867e395f4026a2abce5491246c58fa3`  
		Last Modified: Fri, 08 May 2026 19:28:13 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787e2ea3303efd26f2ebd1fd17d3e3c93889d21d36400b34ca37dcf7d1567da7`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 32.5 MB (32534921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e22e229e7b2f71134509ff05865d82d6405f93b8302312e0d11b7f1f754a7`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 28.0 MB (27976052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42c25953eec95e3852ba5f7794bfc79c73d407e0340587232e04314275068f1`  
		Last Modified: Thu, 14 May 2026 23:57:03 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666330fa191a1e5cdf5e5fa3774cabb7564ba2a56e6c7614f77bffbd59eeba36`  
		Last Modified: Thu, 14 May 2026 23:57:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6744d936e8b486ee50c188d8c4e265e59064f3b2678108f172fd3ec432f358c4`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 29.6 MB (29648010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77ff50a9b8fb1f15708d4a60daccc4827048816ce0e1fe48dfa517f9d5443c3`  
		Last Modified: Thu, 14 May 2026 23:57:05 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cf39711b27d9c418e9c1f41919d74ef3e6183fdcef9d3604f0aacfb03bf8a5`  
		Last Modified: Thu, 14 May 2026 23:57:06 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99c9171764ace7346e66dc1d83fd23b3103bbcaffae3a625395057ad4ee795`  
		Last Modified: Thu, 14 May 2026 23:57:06 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:393b9a4b17251cba8eda9f60ed100b20ecc364bcfee98a4edf013850c2314c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8198377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d37e0f7a4b19ab7c43b0b76db08489c5d00db8ea56c84e4a643828ce6f9215`

```dockerfile
```

-	Layers:
	-	`sha256:978e571616615e31ba632ab09fadad45b0b5b56ec0bed641f4320ca72c7e51c2`  
		Last Modified: Thu, 14 May 2026 23:57:04 GMT  
		Size: 8.1 MB (8144691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4603bae7a3b28da5a9d25dd7ff4b0511d5c20d5c8640c020470512cb9f501d1a`  
		Last Modified: Thu, 14 May 2026 23:57:03 GMT  
		Size: 53.7 KB (53686 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:315a1dea853b1d653d44dbef0e01a6c6cf39fd9cb69ea08e21f7d2e2d34c7c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260366489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b858505cbe2547125fbcbc6a56940ee0c8792154ba9fcf4ba27a502dd7e4502c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:49:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:50:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:50:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 20:50:27 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 21:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 21:30:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:37:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 21:37:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:37:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 21:37:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 21:37:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 21:37:58 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 21:37:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 21:37:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 21:37:59 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 21:37:59 GMT
CMD ["php-fpm"]
# Sat, 09 May 2026 03:02:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:05:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 09 May 2026 03:05:55 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 09 May 2026 03:05:56 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 15 May 2026 00:03:47 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 15 May 2026 00:03:48 GMT
VOLUME [/var/www/html]
# Fri, 15 May 2026 00:03:48 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 15 May 2026 00:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 00:03:49 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 15 May 2026 00:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 00:03:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec2632ee8119dd2f20ca1558eea30c9050dbe76cdeddfc47a82d2a99e3e922`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7eeddeb286b4ad82e04422070cc9d0ea14c8385e61c160fdc6de15d44b838`  
		Last Modified: Fri, 08 May 2026 20:55:24 GMT  
		Size: 109.6 MB (109599289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9201651affe69dbeea0b40dd0a01797ab879ad276cbce7b1035fd2abbe6f32`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da52c1dc2f154f45501a19ca563488fcbdba40ecb1e1594787526100562291eb`  
		Last Modified: Fri, 08 May 2026 21:34:09 GMT  
		Size: 12.8 MB (12758038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd704b420b14b401b979fab20967f6b358b41029a75c95f4618fc304a19abaa`  
		Last Modified: Fri, 08 May 2026 21:34:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b83029bf18b70a38bf0bf5cd859c252a7c004645238124cdc29b5d57f838fc0`  
		Last Modified: Fri, 08 May 2026 21:38:24 GMT  
		Size: 12.4 MB (12440242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb2ade5ab308cb4236ef51bf4896d32c121cdb2d5dac2d45e4cfa02f8c73536`  
		Last Modified: Fri, 08 May 2026 21:38:23 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df2bbf711b4c42b23dc7f14cd3f81187d671d74e56bc882f9796b4c908654e`  
		Last Modified: Fri, 08 May 2026 21:38:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e309ad2e545eabd25f6a6dda72696b904d209d2b06439108d204722a64f342b`  
		Last Modified: Fri, 08 May 2026 21:38:23 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe49513d91f01866ff62fd7d3256cfa600176a1e91fb3f678068a2bc06c7ddf`  
		Last Modified: Fri, 08 May 2026 21:38:25 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3781c334e6e6c24672318769dbf181c195b313e0cde53d3f7927bc2e07f0882`  
		Last Modified: Sat, 09 May 2026 03:06:31 GMT  
		Size: 33.1 MB (33079243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdae0a06433fd0c0b88d4c5d0f0bcf640b36acc0fb852e3fd295c85623b90d3`  
		Last Modified: Sat, 09 May 2026 03:06:31 GMT  
		Size: 29.2 MB (29225277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7e739b9904574bbfbf107828fb0838f2d3ddfe79323403b3307ed75a69c46`  
		Last Modified: Sat, 09 May 2026 03:06:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c383570f16e16c2771db0b823fe45b262f826d3a1bffe27f0e94e675260dc1a`  
		Last Modified: Sat, 09 May 2026 03:06:30 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cbb188a26b38bc8fef8ac0a4cc99cc0acfac8b459f7483f2da7b17aee68875`  
		Last Modified: Fri, 15 May 2026 00:04:21 GMT  
		Size: 29.6 MB (29648011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bfcae4b462b28af8e9229478f3e016fa9bfaed9e6087d57bd041aa86bd4b16`  
		Last Modified: Fri, 15 May 2026 00:04:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2c92df545356ac6cb1ea5f53b402ec634e7dab7c6e55645340bbc45e80a8cc`  
		Last Modified: Fri, 15 May 2026 00:04:20 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302a443da9398adde0d58503de7c6344112d9576a76dcada7a745b474879c48d`  
		Last Modified: Fri, 15 May 2026 00:04:21 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:cda0c660753788ccb944ab39ac385564695569891e5f4282b516e9d019a33f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8226219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b924fa4506d35107cf2250c3ebb86d1d32d54836edd2b05ce8bfb38c9579bf4`

```dockerfile
```

-	Layers:
	-	`sha256:9a4080b8a83bf6496ca7c897fc8719652286266d0c08971e277fc8a7426f22c4`  
		Last Modified: Fri, 15 May 2026 00:04:21 GMT  
		Size: 8.2 MB (8172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ac3786afe8cac3f3ed5429951a57358a5eac41e04d9611bab9c23847792403`  
		Last Modified: Fri, 15 May 2026 00:04:20 GMT  
		Size: 53.8 KB (53825 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-RC4-php8.3-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:95c5d57715231f2706b866eef67304ea971f0b404012ef1aadd0c0705cf36a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235415416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99d388d9d65338d99dfbe15039729a7aeb9a518eedc78dc618115b8c4bce6d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:34:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:34:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:34:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_VERSION=8.3.31
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Fri, 08 May 2026 19:34:43 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Fri, 08 May 2026 19:46:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:46:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:53:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:53:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:53:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 19:53:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:53:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:53:09 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:53:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:53:11 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:53:11 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:53:11 GMT
CMD ["php-fpm"]
# Thu, 14 May 2026 23:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:55:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:55:32 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:55:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:55:34 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:55:34 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:55:34 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:55:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:55:34 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:55:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d1ae8e8dfc4770fdd123ecb7898605c813fac030d26ac659eb819aed4987b2`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152764c8b29d169484010780d4e0129b4cf3928183a3c8aab4689b1efc648a69`  
		Last Modified: Fri, 08 May 2026 19:40:01 GMT  
		Size: 92.6 MB (92573230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b279701afd4f9609f8e7b757e186ed9dbe4cb66b642fd4c8b7b430f8c207dca3`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524cdd703fe86a31e7b10147e47fb1f40ec3402d92d3b33e1542bca5e5e95b30`  
		Last Modified: Fri, 08 May 2026 19:52:58 GMT  
		Size: 12.7 MB (12749861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e187618d8e55df6516d3b1fb3a5de63d11bb35f20491524475976afc859b7220`  
		Last Modified: Fri, 08 May 2026 19:52:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd3efb7855f13a2b9c9f84d8667a384f3b2482dd544741a3ecc72dcbc902fd0`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 11.8 MB (11773502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7482f6352824becde54a0190a9f4d4d9be9002ca50bb857279295866e493869`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553d4bbcbcaec3e0f158f321e6fcdb771e5cfc178445467476e245bf8d607dd2`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7700e2db07b29545fee225564c5662f9c54ed5f29bb14f848abf2883f4389de9`  
		Last Modified: Fri, 08 May 2026 19:53:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a7751494e887571b74b2d86d852ae4f24865898718d5ef4daefd4c97fbbfab`  
		Last Modified: Fri, 08 May 2026 19:53:33 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98085800126cb7a3c991d536861eba59dab1f3477cdf571093803933fab9009c`  
		Last Modified: Thu, 14 May 2026 23:55:56 GMT  
		Size: 31.5 MB (31524299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21fe8ac6ec46e9a41ff7459ca07ac294a8f872a08395def5f824b7bd821ff0`  
		Last Modified: Thu, 14 May 2026 23:55:56 GMT  
		Size: 27.3 MB (27287850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264510b0996da392949ff2af5d111fa03f02edf2ba369ea3b7204a04e5125013`  
		Last Modified: Thu, 14 May 2026 23:55:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706af85229794d1a25a3ef6a3b686f1f2dad1d78e414c3df285903d02b580b6`  
		Last Modified: Thu, 14 May 2026 23:55:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d9dacdf884eb47b42f04708be991cf4bf8bbdade7abdf14f07aa260694387f`  
		Last Modified: Thu, 14 May 2026 23:55:57 GMT  
		Size: 29.6 MB (29648017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be622875b96c00cdb31aa7e851391694f9c3aa835cf25b2419def3704c535649`  
		Last Modified: Thu, 14 May 2026 23:55:56 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9081f84fd055ebf21cb41a360aef6bdf7c511cfe999a17c13b22856e6a6d96ce`  
		Last Modified: Thu, 14 May 2026 23:55:57 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d647fbc6860be380f83c9289d765d6864e00f469620f02ac4fd095a8a23b6aa`  
		Last Modified: Thu, 14 May 2026 23:55:57 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:4eb820eaff90fd1fbcecbabf9967f3c5295478bdf418f95f4293de258ee3089a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7944546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2dcf4484955fcb2dbb98e6526572c6fc467ab90eeb7c492393ff0367fa9701`

```dockerfile
```

-	Layers:
	-	`sha256:aed090019d23db5b99c774892a258148200b70a2e467b03389f995f3eaedbbe8`  
		Last Modified: Thu, 14 May 2026 23:55:56 GMT  
		Size: 7.9 MB (7890807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2903abbc4857d1e048d81baab0f770936c79679505f46358797c53815333a4a5`  
		Last Modified: Thu, 14 May 2026 23:55:55 GMT  
		Size: 53.7 KB (53739 bytes)  
		MIME: application/vnd.in-toto+json
