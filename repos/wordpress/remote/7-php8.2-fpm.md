## `wordpress:7-php8.2-fpm`

```console
$ docker pull wordpress@sha256:900c62455682ce3be421af0ac13f301d095fd80cc4dc40bd82fde161efbf1a3a
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

### `wordpress:7-php8.2-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:a8fb4f9084e6882fbae736f9c4e7b8d2a16abc349a6d5dc3730bc52324753574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264236471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f105d7c65129ae044312381e88f34dd1329f4e67e05c898101f3d745b4aed6d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:28:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:28:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:28:20 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:31:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:31:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:34:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:34:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:34:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:34:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:34:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:34:17 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:34:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:34:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:34:17 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:34:17 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:22:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:23:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 02:23:56 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 02:23:56 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 02:23:58 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 02:23:58 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:23:58 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 02:23:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:23:58 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 02:23:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:23:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1459bb9d852fec3477009c2ca9c040e6d5230132b31ff6c71f70fec2d8adb38`  
		Last Modified: Thu, 11 Jun 2026 00:31:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b1bc189efe3d863678e478e10440aa5bce4644e67f5a647bfeb0842161eff9`  
		Last Modified: Thu, 11 Jun 2026 00:31:26 GMT  
		Size: 117.8 MB (117840065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809ab5a9af90bb893179965ad06e5d9ae761b4edb5e82bf21f3aa491e1c930d8`  
		Last Modified: Thu, 11 Jun 2026 00:31:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962c69c6d9bb995b0419263265bd404b46e139046bf9647a74d4ef1a79749c3a`  
		Last Modified: Thu, 11 Jun 2026 00:34:29 GMT  
		Size: 12.3 MB (12308529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5d47dffd72ef55c715b508ba940c88591cb7b8b5b42baa0e502b8b6b3ae0e5`  
		Last Modified: Thu, 11 Jun 2026 00:34:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fafc6468018ec9bc6ac2e60d0b07d3c2ad6e75e4d8478056689e6824332ff5`  
		Last Modified: Thu, 11 Jun 2026 00:34:28 GMT  
		Size: 11.6 MB (11646428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa3fc8870d656563ad6d2e5c7d1a19e1eb2cfb187e60aff89f88ccf2aaef82b`  
		Last Modified: Thu, 11 Jun 2026 00:34:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3911fad69a60a91eee1966b332607a2e56306a01dfc886c39d0f681d03bdfa`  
		Last Modified: Thu, 11 Jun 2026 00:34:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f2b12ed91ea232c9ac0968117e52bbed70288b51199baf539e8d390d437301`  
		Last Modified: Thu, 11 Jun 2026 00:34:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39744b9d2bb18f87a945b2c249ecad1cc06854cf23fc5efa14d9eaae302225f1`  
		Last Modified: Thu, 11 Jun 2026 00:34:30 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de16f35abb8e2ac0f13931bacc81705b62a87d0883b77e583a43ebd5132095c`  
		Last Modified: Thu, 11 Jun 2026 02:24:17 GMT  
		Size: 33.1 MB (33076909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e18923855324dffe5d2b3e1294ff8fb362a11ae6748db72249732d0ba165d0e`  
		Last Modified: Thu, 11 Jun 2026 02:24:17 GMT  
		Size: 29.9 MB (29911644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf924444025cb429ef2281ebd8bc667653d1525268b18cbc53c1854ed16e09`  
		Last Modified: Thu, 11 Jun 2026 02:24:15 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e31fb7cbc2a620c152baeab1bb8bd205812571a2ee5ba4771aeeef8045903b`  
		Last Modified: Thu, 11 Jun 2026 02:24:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cf35c72137811f9c06511313effa06bb6cc756a2f8af59e9ad5d8ab40b9f7a`  
		Last Modified: Thu, 11 Jun 2026 02:24:18 GMT  
		Size: 29.6 MB (29649208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9679eea8776208c3c0832b6e5ed35e0b098d478ee1d699c28e4e5b3b76b909`  
		Last Modified: Thu, 11 Jun 2026 02:24:17 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e80af43dab266cc437a4b589e98b76e8c3e66692dd64d92527ee3d1539b42ab`  
		Last Modified: Thu, 11 Jun 2026 02:24:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12bb8ef745c9b796ea9b061be5247935738819f09b0a87026770c1bb7ea757`  
		Last Modified: Thu, 11 Jun 2026 02:24:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:cba77db05ace163523c5dcc24d3253a0178a4769a85b9644c91692f364ced0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8222965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca73a4cbf86b19313ef20d10a7d4cf5dc40f8e0925e2d12da63ce903747cf5c9`

```dockerfile
```

-	Layers:
	-	`sha256:b0c62ae1fbf2ba750cdd4590b011aed34b804492f1f823a8eed6aaa9dae16153`  
		Last Modified: Thu, 11 Jun 2026 02:24:15 GMT  
		Size: 8.2 MB (8170523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc809f19ac00c2809562ca867acfaaf8c0396098c965e8cc5a773b7749980333`  
		Last Modified: Thu, 11 Jun 2026 02:24:15 GMT  
		Size: 52.4 KB (52442 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:ee2d4c53f2b99b55036dd971ad3498202582c38080fbbc8700b0bf0a1e651995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232822691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c030665c14723cc63ee09da337c96799c949adfa6bdfcb625584b0d40402c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:16:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:16:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:16:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:16:28 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:41:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:43:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:43:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:44:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:44:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:44:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:44:00 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:44:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:44:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:44:00 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:44:00 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:43:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:45:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 02:45:55 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 02:45:55 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 02:45:57 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 02:45:57 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:45:57 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 02:45:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:45:57 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 02:45:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:45:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6872858e05906f41801f4e7315a56050d1dbd264d0d5561166f13a06d425d1`  
		Last Modified: Thu, 11 Jun 2026 00:20:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d8c3c60558bc383fcf4d60105565f13a7bd3160d0c33266373d9f0156fa21f`  
		Last Modified: Thu, 11 Jun 2026 00:20:27 GMT  
		Size: 94.9 MB (94885875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40b0ca72a3c906a5f494b8b14bcffb2c50931a0b82efd5fc8c804377e61b68d`  
		Last Modified: Thu, 11 Jun 2026 00:20:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2f01ea08436bccdf5df118ead4ab8dd44e6df9af6737e25fbfb13e53ee426`  
		Last Modified: Thu, 11 Jun 2026 00:44:11 GMT  
		Size: 12.3 MB (12313032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f461b150666123bf7a6d264b274e144d1962f2615d6b369cc29d45a3f5b97`  
		Last Modified: Thu, 11 Jun 2026 00:44:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033d4632fcc87baa6612050a58fc57b37cf6f43cc2b6a15d578634814780aa0a`  
		Last Modified: Thu, 11 Jun 2026 00:44:10 GMT  
		Size: 10.5 MB (10462006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c415023c75130c5f4a962510f199289e518813c8af949a705ee4537eed8a7f`  
		Last Modified: Thu, 11 Jun 2026 00:44:10 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bdcd754f6fa3ace650b661448220f775b17870bcaaeabe288bed8272789a1`  
		Last Modified: Thu, 11 Jun 2026 00:44:11 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec42bf8ace6e2e94ca9ce953f81c229f316b158c5dba379bf3f50a8c6e3bc5`  
		Last Modified: Thu, 11 Jun 2026 00:44:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4568717934735fe92a371becfa7a99937987721c9216d37ed496d8fd2be8d506`  
		Last Modified: Thu, 11 Jun 2026 00:44:12 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c49aa8a7f4a7ee190caf6047d4bcda5e318e0d444bf4339cc608786587e5387`  
		Last Modified: Thu, 11 Jun 2026 02:46:14 GMT  
		Size: 30.3 MB (30252654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6e41f0ba94312c2b2012c374486caad033187c4f55ba349e5469d1f1ceeaf3`  
		Last Modified: Thu, 11 Jun 2026 02:46:13 GMT  
		Size: 27.3 MB (27282434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f0647fd15dbacc49fa1256ce4f46277e584b9b8bd2a002eb214d438ae18bf2`  
		Last Modified: Thu, 11 Jun 2026 02:46:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03c086eab1f818926b9686ef337c0468af44ff6e747442cbad14818edc7402c`  
		Last Modified: Thu, 11 Jun 2026 02:46:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49710e119ce0f4729021262e728bd5550b8abf672efd7dcd749519e4d1a410f8`  
		Last Modified: Thu, 11 Jun 2026 02:46:14 GMT  
		Size: 29.6 MB (29649203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c92f33cc664e2aa7cd3ceef7565976b0df210d4fe8b19ea4f3bfd260dd1aa`  
		Last Modified: Thu, 11 Jun 2026 02:46:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf973111c85a50893dbcab59db4360530fc89bc5d884f79840348a975a991848`  
		Last Modified: Thu, 11 Jun 2026 02:46:15 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02c10178f35283d7cfd4e859f06c2feda23cc4ffee7a03397a319b35315045`  
		Last Modified: Thu, 11 Jun 2026 02:46:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:f01047f64ad63cade4fd178b1e7d03c1c205db6e2836d6ecc19a244e6c2293d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8016614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1c79fd692412f4c63c51fe2d6883c5235e5d5f79ee9c2368944ded029537f`

```dockerfile
```

-	Layers:
	-	`sha256:240e9e9107744e5972cef27dcd9d091cb5fe24557dc023550dc9f2a7d274f694`  
		Last Modified: Thu, 11 Jun 2026 02:46:12 GMT  
		Size: 8.0 MB (7964036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c7a3722bc99eb234d80f82a4a1ed96329e28bda23230e081eb5327764447a9d`  
		Last Modified: Thu, 11 Jun 2026 02:46:12 GMT  
		Size: 52.6 KB (52578 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:2de6fa9f54621fa21e26c0aea98f9b38f15e72918fec54a698e81a78fcfb630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219146842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3155cfd79238a91817564197dfefcf2fbae3cfc1facce9978a8ae85d0a134bd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:25:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:25:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:43:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:45:56 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:45:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:45:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:45:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:45:56 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:42:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 02:42:20 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 02:42:20 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 02:42:22 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 02:42:22 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:42:22 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 02:42:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:42:22 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 02:42:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:42:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a5096c8e315268d2e6e3c3324a9b6a68b349959f9c1321bced1c8ce4e6508`  
		Last Modified: Thu, 11 Jun 2026 00:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b51cc1d4e0fad8159186b5df96c242bb4ab64e6f8dd8dfff388b824acd9e6f`  
		Last Modified: Thu, 11 Jun 2026 00:29:21 GMT  
		Size: 86.3 MB (86255562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dd2c90ceba4df47e0f9b43e63fba9a63557f2ceb0d1cd7d8d831172ba11b1a`  
		Last Modified: Thu, 11 Jun 2026 00:28:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe7e1cd8b190d3ecf3d67dff01b87f08bddc14dfa25f687f44dd8d3daac6b85`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 12.3 MB (12306127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41855ab0079076a07a5acb03bf45c82fef99024d4b5ac497db6a184f8eb47823`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b943382aed163eca8b2da0c9a9528dbf9db4c10451b2c098ac7e3e77b7a8b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 9.9 MB (9859582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef59b64cb3c76cda6bc4020cf9edfe0a2dd15f6630418392e2bc433f37cd3b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c18ffead64caf4f9583401a0f25f14a965bac16b44b8aa9e9c784d27a8e515`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c10dfe7d85cd2e12e406fff4d00bb9d0fed8aa27ac4b0184d2ab5ffda5cad90`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e33ecd119ec3afa19677a826e20b12cce8fb06e0d9551ed51adda38317999`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b90b652120cd07ebe450b5ed07d5f78ea2ea1a9b59eeaa98560f928559616c`  
		Last Modified: Thu, 11 Jun 2026 02:42:38 GMT  
		Size: 29.1 MB (29133194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f015ec4aad7766f59a89f999eec8b0d6e8ba73ad985c84933be520e8a5982f`  
		Last Modified: Thu, 11 Jun 2026 02:42:38 GMT  
		Size: 25.7 MB (25713895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e785e2ca17f606e58930428219a08924ecb7b7a0a6ed75b6cfcd9db74b7a14`  
		Last Modified: Thu, 11 Jun 2026 02:42:37 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5454fa031b4f255e3b054728de909f01492dc45b48dcba75e5c9516dda076d20`  
		Last Modified: Thu, 11 Jun 2026 02:42:36 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643bab7f3635b335a66e13ae04e73e3812fa10eedd35d3e92dccfb9e52549621`  
		Last Modified: Thu, 11 Jun 2026 02:42:39 GMT  
		Size: 29.6 MB (29649204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc32cdedb24eac3c5f115f3db06fcbca2134bfbea982000879c23b84b7f9991`  
		Last Modified: Thu, 11 Jun 2026 02:42:38 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fedfbd28f5567b9d6ceed266fb950dba7a9f7e95a80efa56373585d2ab70e49`  
		Last Modified: Thu, 11 Jun 2026 02:42:39 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9282eb0984fb0ead149f8be59eb01fa8e9ca300f528047f63919378081fe8`  
		Last Modified: Thu, 11 Jun 2026 02:42:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5be79e2609f71b8090d28db527d1fe9888f0ff58d021ca0898ae9c03380e73f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8021411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe218fdf7f17ffa400732c4b1240fef1259ce07b62458373543b8fe2c93613d`

```dockerfile
```

-	Layers:
	-	`sha256:f189c36740801e67789c45d4f663d16b5c683c17679e8b688b2c706dc9110eab`  
		Last Modified: Thu, 11 Jun 2026 02:42:37 GMT  
		Size: 8.0 MB (7968842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0cbb7d5a2a3c79fd9207d36c54d86895edaa302f920be358302f6788f9d78e`  
		Last Modified: Thu, 11 Jun 2026 02:42:36 GMT  
		Size: 52.6 KB (52569 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:d8cf0f64b1c74d079351d114a401990af731c3b0c4018502b783ad880636286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256795282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04033756dfadd14c172dfd5e62b5a20045d73f5b30723a486e3f7b409b0e98ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:24:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:24:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:24:24 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:32:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:32:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:35:22 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:35:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:35:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:35:22 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:35:22 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:23:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 02:23:26 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 02:23:26 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 02:23:28 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 02:23:28 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:23:28 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 02:23:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:23:28 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 02:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:23:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd68c68bd2c9c5026a0f0d64dc4f9ba0977234322ed6fafa235bcdbf17dfa4`  
		Last Modified: Thu, 11 Jun 2026 00:28:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc996dc8a38d3e4c58fa4f08b9f5252b36d397c0a5df8d99cc972e938b40e85`  
		Last Modified: Thu, 11 Jun 2026 00:28:07 GMT  
		Size: 110.2 MB (110168631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4836bb3e1dbe32d6ed4ca04dc935afc686f259e9b4edb74cea8b720339e40d9`  
		Last Modified: Thu, 11 Jun 2026 00:28:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7bb9d3ba585cb751da1a01cdeb4048da2a45129b2f9586cf272904af6e08a`  
		Last Modified: Thu, 11 Jun 2026 00:35:33 GMT  
		Size: 12.3 MB (12308144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311605bb6dff44641f3b5ec72738f76cb215676136d7f34c78d13aeeb4b1bd4`  
		Last Modified: Thu, 11 Jun 2026 00:35:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0216ff71249189a3c813ca72986702daebac2b1e5bc29398c499b1af0bca8e7`  
		Last Modified: Thu, 11 Jun 2026 00:35:33 GMT  
		Size: 11.7 MB (11686708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b122e152c62afa3ce18daece9a62f7a52e0a538f1acb18bf6aebc2e1575551f3`  
		Last Modified: Thu, 11 Jun 2026 00:35:32 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f49af6a2cad4e9930ed6b0298825c99bafca5f1cb1c34cf35f52d5f1b982de`  
		Last Modified: Thu, 11 Jun 2026 00:35:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ccedb2fd3be5eef335624f4747151ac41ea7634c7a0da101a10539ab72e0f7`  
		Last Modified: Thu, 11 Jun 2026 00:35:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968e04ceb78c37a8aea114da8a266178c52b5672626b48c1a0d78b6564710476`  
		Last Modified: Thu, 11 Jun 2026 00:35:35 GMT  
		Size: 9.3 KB (9256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f627a7553c241f5fa03ee2aa9912dbe816c7b34f14d5de2dd8170a09b44b1`  
		Last Modified: Thu, 11 Jun 2026 02:23:46 GMT  
		Size: 34.6 MB (34580462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8e4e7296faa0ee8743819b87517fe7b17c7e3ae067b7ebd61927aaeb9e1457`  
		Last Modified: Thu, 11 Jun 2026 02:23:45 GMT  
		Size: 28.2 MB (28235329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa407d677429403323bed82874044ccf0cd15e88ce4955ad554157404fe15f`  
		Last Modified: Thu, 11 Jun 2026 02:23:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8993c863fa1c4f9249b975c51e1a9ad1d33fad03c8f7ec8adb0e6d76a636ecb6`  
		Last Modified: Thu, 11 Jun 2026 02:23:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c884eaadf2dad948f1648ae98d22c0ff656fde55540be8a681ea033d3f3be6b`  
		Last Modified: Thu, 11 Jun 2026 02:23:46 GMT  
		Size: 29.6 MB (29649202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035cb5f9162d68fdf6ac46505456c5bb259517db2e862ecf0fd849f60d41dd5`  
		Last Modified: Thu, 11 Jun 2026 02:23:46 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3912a23286d98f2bb573deaba0a200418d87dc516f917818f3d96eb794b672`  
		Last Modified: Thu, 11 Jun 2026 02:23:47 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db76889d5e1df97d9a5f5b1f2e48c1bc1b268f54bdaed474b9ed7f9898501425`  
		Last Modified: Thu, 11 Jun 2026 02:23:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:d384393da41a14bb09ca46c5354f17675f4ef1548561005e9a019096b78b4be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8319592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390a3f13306018d945951da329b0e15a1499d6e181a67697e176c8d60837d564`

```dockerfile
```

-	Layers:
	-	`sha256:4f955a3cf0a871deeeed454fad841223efe76c85431ba67e4be62508a0294df5`  
		Last Modified: Thu, 11 Jun 2026 02:23:44 GMT  
		Size: 8.3 MB (8266971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36275078dbe09c1fae647a16d54eb6b7bb22c1912b5bd4edac2c4063192c37a`  
		Last Modified: Thu, 11 Jun 2026 02:23:44 GMT  
		Size: 52.6 KB (52621 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:fccf2033bfb2e5f357c1fea7dcd0f7103c20548f6ee586bf0b096bc4bb0513c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261796187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9aac314224c05187274ea1adb3f91e7fa358d938f35445ccb77be95fbae74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:28:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:28:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:28:56 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:29:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:29:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:31:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:31:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:31:34 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:31:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:31:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:31:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:31:34 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:23:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 02:23:52 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 02:23:52 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 02:23:54 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 02:23:54 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:23:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 02:23:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 02:23:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 02:23:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 02:23:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a7eed8f2a624e80c598f2e5aa51eae4ff8a389539027ed26f2bc2f01f5ed9`  
		Last Modified: Thu, 11 Jun 2026 00:31:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e1154181e6b8a3aea55153e1a15f0f03f2bd8d13486b0229a5bbfbaa8769cf`  
		Last Modified: Thu, 11 Jun 2026 00:31:56 GMT  
		Size: 116.1 MB (116142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ccf56b7152391ae5e6a2655154b5482c0a105d90804e37117f84c7b5ae2eca`  
		Last Modified: Thu, 11 Jun 2026 00:31:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8002fa626e68de580a7a5e52a1add1f67a08a962d14d38ec64a888d0050e6867`  
		Last Modified: Thu, 11 Jun 2026 00:31:53 GMT  
		Size: 12.3 MB (12307447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d3a3a7741835cbe13d392be475391827d36e15671965905c31a8b96ee19859`  
		Last Modified: Thu, 11 Jun 2026 00:31:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61662cee4233951342d03bb4a0be8b9150da589483946cfc9ce517d7134e8d00`  
		Last Modified: Thu, 11 Jun 2026 00:31:55 GMT  
		Size: 11.9 MB (11871035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e6849482252577eaa0f8dcfd16273971dadc49d3150d670758a4b54fb5322`  
		Last Modified: Thu, 11 Jun 2026 00:31:55 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2f3aa42004bff182fb4353850bf904486f7b26bceb3a644908feeccd24296a`  
		Last Modified: Thu, 11 Jun 2026 00:31:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad60438f8520224651866ba3f15fd8059d26a0b139fea95c543028ddba64e1af`  
		Last Modified: Thu, 11 Jun 2026 00:31:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6243a3efd3dbc3095e0d18bd4d5dacbba2e7fa4219eaab16b8df543c6d197fd7`  
		Last Modified: Thu, 11 Jun 2026 00:31:57 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f176345760feb5b92d03f63b58a670068d774b29ad5d43e18ea348b1f2510645`  
		Last Modified: Thu, 11 Jun 2026 02:24:12 GMT  
		Size: 32.5 MB (32535068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dc3d8b691e0749c60c3a8ea2fa5edc2283200409475f7043fbeb7f9f8a8af2`  
		Last Modified: Thu, 11 Jun 2026 02:24:12 GMT  
		Size: 28.0 MB (27971643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9d6ce2f7a1811aeb50bf6ca21a678d4d42457041367eb982b31c91f553a30`  
		Last Modified: Thu, 11 Jun 2026 02:24:11 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992c34cd8722fbda11541b165750d6dcafae5651995444ef9c7e8f26e40ff39d`  
		Last Modified: Thu, 11 Jun 2026 02:24:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b535eabdc02e24f93c76e713f785f45f0919ede25a76fc56fd4a8be1aa15aa`  
		Last Modified: Thu, 11 Jun 2026 02:24:12 GMT  
		Size: 29.6 MB (29649200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a2884321be808ab4163eb13044235c7652529eb407efc77b584c4a2951401`  
		Last Modified: Thu, 11 Jun 2026 02:24:12 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46277b1aaf846ae42e3b4d381b05f5643246cb8e7c0b8c2fc82542db60981a6a`  
		Last Modified: Thu, 11 Jun 2026 02:24:14 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7331fa0c3ba84b79d08339fda2d104d3a4558c040dc461fd769d37bf1e144551`  
		Last Modified: Thu, 11 Jun 2026 02:24:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:c5ee6cb6de6565d54615892c9a317ead1d06c979914ad23fa21b2decbd94da06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8195975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913d8222e66cfd42678786cecff438dea77653847178a2c44770022e148ee589`

```dockerfile
```

-	Layers:
	-	`sha256:f70d01c112ba9dcc643c16f51f7d88f522b8ec12ed77c507b6fddded7dccd7c6`  
		Last Modified: Thu, 11 Jun 2026 02:24:10 GMT  
		Size: 8.1 MB (8143575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46a985cf37101c60eaa51cbb292b7d1d5f4769e6b060ca0346d1b75f0090699`  
		Last Modified: Thu, 11 Jun 2026 02:24:10 GMT  
		Size: 52.4 KB (52400 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:bd7492580489972e8f7fbf150671f06805b995b9c2ebd3684dc20ded24df0e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259665431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3dd568dfbeeb7e0eb6447bfe73d2d650eaaee5b0ea8f2ec772c65e50aaf01e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:26:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_VERSION=8.2.31
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 20 May 2026 00:29:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 00:29:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 May 2026 00:40:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:40:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 20 May 2026 00:40:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 May 2026 00:40:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 May 2026 00:40:23 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:40:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 May 2026 00:40:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 May 2026 00:40:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 May 2026 00:40:24 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 06:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:28:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 20 May 2026 06:28:49 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 20 May 2026 06:28:49 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 21 May 2026 22:55:43 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 21 May 2026 22:55:43 GMT
VOLUME [/var/www/html]
# Thu, 21 May 2026 22:55:43 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 21 May 2026 22:55:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 22:55:44 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 21 May 2026 22:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 22:55:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651a003498bd50572d1189161afddcb900241800cb6d5d0bd7a8ce4500633e3`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8ec5f6bfff3150dfdb7f9ba59b5b8bbd45b012ab504b03e5eb22da1815753`  
		Last Modified: Tue, 19 May 2026 23:31:29 GMT  
		Size: 109.6 MB (109598335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c429ba9d511a0b12b2e87806d0728dcd1c7b4dcadf247dfaf38502d93c30cd5e`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab05e99524ea8a310f7e5416beb5cfe3530cd3f44900215f78710cba5a5836bd`  
		Last Modified: Wed, 20 May 2026 00:35:05 GMT  
		Size: 12.3 MB (12307518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd8eb106e81228aee1db8677bd8aac733059b3aa00e61112cefcd2ae4b645ec`  
		Last Modified: Wed, 20 May 2026 00:35:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599dbabce281d2af9ed07a97b2300805bdff87da2527a9b54d21ede573b3dd16`  
		Last Modified: Wed, 20 May 2026 00:40:46 GMT  
		Size: 12.2 MB (12191303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff51d0849df41525073fba38df81f1f45bde6b03309ad55ee4e68b4bdd65220`  
		Last Modified: Wed, 20 May 2026 00:40:46 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407ae59d1a16412af96202ca4e368a762797cf41b45c0e6c40db81b85d1ccc1`  
		Last Modified: Wed, 20 May 2026 00:40:46 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70564b9e762c43536add1227d360915ebc9baad1d59d10b8c2da9f5725f3502d`  
		Last Modified: Wed, 20 May 2026 00:40:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934e9c3f9ea47c2204155b97ecf85b693763abc63a332ebdcda85287def443c3`  
		Last Modified: Wed, 20 May 2026 00:40:47 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec461d5b83b23e7a0a37bce7157f884db1edb0320e18935ebb0a42523d88e48`  
		Last Modified: Wed, 20 May 2026 06:29:30 GMT  
		Size: 33.1 MB (33080105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e889aefed430685c3f8b945a416d7fb61ebee6bd760882195715cfe021e9509`  
		Last Modified: Wed, 20 May 2026 06:29:30 GMT  
		Size: 29.2 MB (29220217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90d5ad2a3f71d77b00046a2584b5e5c9bd924197a2c037dfec52ef6bbf4edf`  
		Last Modified: Wed, 20 May 2026 06:29:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8086ee4cb75ad7c69db1337fd8735af16249b7f157ab69753d5d23a757517b`  
		Last Modified: Wed, 20 May 2026 06:29:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f7e2c9f6f67b01d6d673fa800d3f36372b6dabb6621128e9e48cc60bd96f44`  
		Last Modified: Thu, 21 May 2026 22:56:21 GMT  
		Size: 29.6 MB (29649203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbbedc086a5bc266477a7e977776308ee3fba6b1a9b8516cdadf0a3c9b051b9`  
		Last Modified: Thu, 21 May 2026 22:56:20 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1508e0c0c6d3b3910c2172c69755eeb7a353d40939a9fae259610106487bbd4e`  
		Last Modified: Thu, 21 May 2026 22:56:21 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c36b8d6434dbeeb8dcc8577ba955f2cca0124bea96d4c185d6805e099b0dc42`  
		Last Modified: Thu, 21 May 2026 22:56:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:64fb44ca267ac3688df4e7a6bebdc1ff3efbcbb7ad8fb1371634d713bdf9e458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8223676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf43953bfa6d17aa1f9427427e64c6d85046f065c0ea9de4d06a5d364b6304b5`

```dockerfile
```

-	Layers:
	-	`sha256:59fe8a2e4d88133d4b7b05bf5ea1b9ad7ed68f48f273e70f6883dc6d75e27524`  
		Last Modified: Thu, 21 May 2026 22:56:21 GMT  
		Size: 8.2 MB (8171180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beab6ffaec7f169b8002d62a885a6ef5acbdd0223b4221c1b7e2a8895a8de9f5`  
		Last Modified: Thu, 21 May 2026 22:56:20 GMT  
		Size: 52.5 KB (52496 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; riscv64

```console
$ docker pull wordpress@sha256:82b8b1a5d2fe5f5a70294edd18dccce4892ed0bd62aed6d91daa7693694574ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285159455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21e39f2f08ac417779022f7df6cac3155f69c2da4137d861e4a0f6b73326df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 11:59:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 May 2026 12:01:47 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_VERSION=8.2.31
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 20 May 2026 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 23:30:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 May 2026 01:57:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 May 2026 01:57:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 May 2026 01:57:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 21 May 2026 01:57:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 May 2026 01:57:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 May 2026 01:57:32 GMT
WORKDIR /var/www/html
# Thu, 21 May 2026 01:57:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 21 May 2026 01:57:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 May 2026 01:57:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 21 May 2026 01:57:33 GMT
CMD ["php-fpm"]
# Sat, 23 May 2026 03:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 May 2026 04:03:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 23 May 2026 04:03:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 23 May 2026 04:03:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 23 May 2026 04:03:12 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 23 May 2026 04:03:12 GMT
VOLUME [/var/www/html]
# Sat, 23 May 2026 04:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 23 May 2026 04:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 23 May 2026 04:03:13 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 23 May 2026 04:03:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 23 May 2026 04:03:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3f1ce6bdb422619d5f28f3d354ac88efadf525446aa4cc0a2cf6d208358da0`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2278d8aba6744e8388864d93d2ccd060b4b5b706da0855420292afc7562eef8`  
		Last Modified: Wed, 20 May 2026 13:05:36 GMT  
		Size: 146.6 MB (146584901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f680f6a3aa4a44306703b8a92e46d186729d6e1435771fbfda06e18de5ebcc5`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14c4f5dfec091391f34886671ff45efb4a6539787803f32c703a461b69583ed`  
		Last Modified: Thu, 21 May 2026 02:00:28 GMT  
		Size: 12.3 MB (12322660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e36a1cff50987b8baebd261749dcba0cdc475ed24c3c3a2741627d459ddad9`  
		Last Modified: Thu, 21 May 2026 02:00:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2fdfa46586ef16a6eb2c1639f61a08779714dae7685f53b278ef9aaf128c97`  
		Last Modified: Thu, 21 May 2026 02:00:28 GMT  
		Size: 11.0 MB (11004699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f094a6723d041f476a6b2a9331c14e8ca5b0c00ceded707e52f797255b667c29`  
		Last Modified: Thu, 21 May 2026 02:00:27 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc28cc367a99bb4ad12f85593c1657e7e6528704a9c7dfac8d5136c5644ac3c`  
		Last Modified: Thu, 21 May 2026 02:00:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ed1916a697503e71da3324e8fb890423d583d0f28648ce83eac1104e6dd7d`  
		Last Modified: Thu, 21 May 2026 02:00:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c965cd986d53f670bc4b373d17ee4d20c3e86fe0dc35df62d5af16e6c51d6`  
		Last Modified: Thu, 21 May 2026 02:00:30 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125cef1362333d54e26e97f682f3171cfade60f0f5bfe6765feb4b64bb7ba61`  
		Last Modified: Sat, 23 May 2026 04:07:41 GMT  
		Size: 30.6 MB (30647869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fa5db9d5c778806beab61e4d49b8ec753192e9701a080d28e50df4d8dbb2c2`  
		Last Modified: Sat, 23 May 2026 04:07:40 GMT  
		Size: 26.7 MB (26654223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a3ae6d67eae2e8fa2e898db02e7748086f018fffbe41bc1046b8626485e19`  
		Last Modified: Sat, 23 May 2026 04:07:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3d936cab9e7b24a82755f2002a8b8bfe715e5e985768d18a72480925528f35`  
		Last Modified: Sat, 23 May 2026 04:07:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f82d80aab070fae542320685237fc178292f60cb2b6fc9a1833bf2c165b4a3`  
		Last Modified: Sat, 23 May 2026 04:07:42 GMT  
		Size: 29.6 MB (29649206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e800f8310e9d4d4546c8e265f4084c9f6325ed9095831b35efeaa1086836a`  
		Last Modified: Sat, 23 May 2026 04:07:32 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6338d67c54c61329a4fb8033a5e7f8ea2d4bbb4b0adf2b2de7afd1b1fe0640`  
		Last Modified: Sat, 23 May 2026 04:07:34 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2435f03b21d9c4f9fe4032aa65b1a69ee0b76eed606675dcf3942f6376dd6e`  
		Last Modified: Sat, 23 May 2026 04:07:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:ef7f48521dc70bd5f89624bdc829083b946fef2d59f1fae41230f547e6a0de74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8288599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe3c33a47507adb76317f9267f6a3861fa7c917aa67f6544b4e2c309b037acf`

```dockerfile
```

-	Layers:
	-	`sha256:4d6c339f664017174bccd44e7b1b2a43f2e7a5d9b026a99d3d6602e51d2c75f6`  
		Last Modified: Sat, 23 May 2026 04:07:31 GMT  
		Size: 8.2 MB (8236103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6471bda5d4815f062049055000db704ad45643c86cc959336bc79720855b7312`  
		Last Modified: Sat, 23 May 2026 04:07:29 GMT  
		Size: 52.5 KB (52496 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:7-php8.2-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:45efd8c1e716e531ea17bfaeb91f3484d9c6d1514fc33044a5924d9b92020f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234742267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa1c3e428114c93f3bc7bec1f2c017c5895b69cc12e405152009230564f69ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:23:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 00:50:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:50:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:56:36 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:56:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:56:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:56:36 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:56:36 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 03:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:22:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 03:22:18 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 03:22:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 03:22:19 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 03:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 03:22:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f12811ca8054d10a6d855c99328a1f0623889381d202bba7392d112bc3de481`  
		Last Modified: Thu, 11 Jun 2026 00:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c3c60b41e88a2039142613d746976cbbd5c2d61145b36679028c24bf550936`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 92.6 MB (92573159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39530e62e350f67cad534ea575f3024d4018b676be4212ebd0ff185c2f12e154`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6966faf644690051635df21d3a3e217daafefb52ad1eacec3a3ae5b209706b0d`  
		Last Modified: Thu, 11 Jun 2026 00:53:40 GMT  
		Size: 12.3 MB (12306830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2a472fd54623274f0ef48e57c304032cc8493ef53598432e6dc742eb3bb88f`  
		Last Modified: Thu, 11 Jun 2026 00:53:39 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6959963a927e2af812cbaf0c1eee64f75b0aebda05e67fc6a3b0b92b48cb589a`  
		Last Modified: Thu, 11 Jun 2026 00:56:53 GMT  
		Size: 11.5 MB (11534365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fefcc447f44601906ec80614dc6a936fdbb3ae261de83bc1fe4fe3de083933`  
		Last Modified: Thu, 11 Jun 2026 00:56:53 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fbc94c5fc32f1e6fe586ea643486e80ff390db3f189aa9eb831ed86c36be7c`  
		Last Modified: Thu, 11 Jun 2026 00:56:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdf69e096b7e84bdac7aeb87c5180af8748bd8c7c266ca8924fd739dff7e264`  
		Last Modified: Thu, 11 Jun 2026 00:56:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d0cc0a38e3ce6b1af2ec66bffc80b602fe43c789667a4ecdf090ab40b551b5`  
		Last Modified: Thu, 11 Jun 2026 00:56:54 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa76e4875691b12e4253348e709497288316a05995d3d93f9eb75452a17ec768`  
		Last Modified: Thu, 11 Jun 2026 03:22:45 GMT  
		Size: 31.5 MB (31524226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f4f53d35d0f509e8ae0a79a2ee2c4eb8c2ea1a47c0b6af11782b3ff8b1efdc`  
		Last Modified: Thu, 11 Jun 2026 03:22:44 GMT  
		Size: 27.3 MB (27284839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3d4dd111b25ad2b1fecaca0cf34ba012bbca6b0e364422b82bebe82253c7e7`  
		Last Modified: Thu, 11 Jun 2026 03:22:44 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7a080de91855858b4684f7907110520333a930a729bcb157d12f020984bb02`  
		Last Modified: Thu, 11 Jun 2026 03:22:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecf682c92c7769ef24c94f74d35e3cda64c9424b1712997690530df60179507`  
		Last Modified: Thu, 11 Jun 2026 03:22:46 GMT  
		Size: 29.6 MB (29649206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bb11c40dc58171553b5c01f47add5817b85fb281e82f1d343412abf82d68a`  
		Last Modified: Thu, 11 Jun 2026 03:22:45 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e887a477713f044a22e6d9c12d1cb41a12cd5b246e22ff2d8da9a5669770fd5`  
		Last Modified: Thu, 11 Jun 2026 03:22:46 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9e2f64ac367fb1f0546cfb61216a6e703ad90962f26286bc5dac7094dbfdc`  
		Last Modified: Thu, 11 Jun 2026 03:22:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:7-php8.2-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:83a38b4f3cec514314e4fd788e23c75d5ff606729a96df42b71fed3fc077f7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7942104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f2e83c091206640972758eb95ba337e34e847afe200d9710fd1d10edea3f8d`

```dockerfile
```

-	Layers:
	-	`sha256:8de5ada39e53d795e3e4cc20c27f79b96c0d72193d00a5b1efa10fd7307ae520`  
		Last Modified: Thu, 11 Jun 2026 03:22:44 GMT  
		Size: 7.9 MB (7889671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6f40c066cbf3af15e5b9d876911d70275522d778374ed8f99d86f77d22960a`  
		Last Modified: Thu, 11 Jun 2026 03:22:44 GMT  
		Size: 52.4 KB (52433 bytes)  
		MIME: application/vnd.in-toto+json
