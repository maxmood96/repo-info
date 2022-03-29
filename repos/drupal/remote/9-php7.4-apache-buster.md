## `drupal:9-php7.4-apache-buster`

```console
$ docker pull drupal@sha256:d62e296150a9ba70beb3192330fb7aded8867df98c5d4ecf4f736d4b46678483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:9-php7.4-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:fe43ef9c8f83bc55b4164d973873e38aa6fe5b731c8299d448e8c76fca0e96a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166847148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fbf0284c28fcef3a42053f2bc82f9f70f369789442bb73baf1670255d850e1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:12:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Mar 2022 19:12:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Mar 2022 19:13:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:13:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Mar 2022 19:13:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Mar 2022 19:21:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Mar 2022 19:21:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Mar 2022 19:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Mar 2022 19:21:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Mar 2022 19:21:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Mar 2022 19:21:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 19:21:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 19:21:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Mar 2022 01:56:17 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 18 Mar 2022 01:56:17 GMT
ENV PHP_VERSION=7.4.28
# Fri, 18 Mar 2022 01:56:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Fri, 18 Mar 2022 01:56:18 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Fri, 18 Mar 2022 01:57:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 18 Mar 2022 01:57:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 18 Mar 2022 02:00:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 18 Mar 2022 02:00:45 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Fri, 18 Mar 2022 02:00:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 18 Mar 2022 02:00:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Mar 2022 02:00:47 GMT
STOPSIGNAL SIGWINCH
# Fri, 18 Mar 2022 02:00:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 18 Mar 2022 02:00:47 GMT
WORKDIR /var/www/html
# Fri, 18 Mar 2022 02:00:47 GMT
EXPOSE 80
# Fri, 18 Mar 2022 02:00:48 GMT
CMD ["apache2-foreground"]
# Sat, 19 Mar 2022 15:26:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:26:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 19 Mar 2022 15:26:29 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Tue, 22 Mar 2022 22:24:55 GMT
ENV DRUPAL_VERSION=9.3.9
# Tue, 22 Mar 2022 22:24:55 GMT
WORKDIR /opt/drupal
# Tue, 22 Mar 2022 22:25:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 22 Mar 2022 22:25:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b26e8f4a602dab7861852544d8e7046aee684a7793de7881f1dc0228729cec`  
		Last Modified: Fri, 18 Mar 2022 04:53:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9936c807db3e0b70025d4882a6d3107723314b8b1d6fe596e5f0a7744ac22f98`  
		Last Modified: Fri, 18 Mar 2022 04:54:08 GMT  
		Size: 76.7 MB (76681203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4834c71afebf16f1f46c5451077b46716db24f2ad9071dc2b31bc16f65cc4dde`  
		Last Modified: Fri, 18 Mar 2022 04:53:47 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b066810508b86caed7662e806f69d572e6ac232a472962e0b1d9175616da7c`  
		Last Modified: Fri, 18 Mar 2022 04:54:31 GMT  
		Size: 18.7 MB (18681730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6237bf8100d5c114ff899ac68a3ea0749f80a45a1a9af81f666388e061fcc5c`  
		Last Modified: Fri, 18 Mar 2022 04:54:26 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378f37f3c0c53d1af9df013492dbcaca37e1799c5a14ab221927ed82b61c4dc0`  
		Last Modified: Fri, 18 Mar 2022 04:54:26 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959675477a2fd4a6b6ca0ba032933cc1ba84edaeb983124a887c1b961995c9c6`  
		Last Modified: Fri, 18 Mar 2022 05:13:58 GMT  
		Size: 10.8 MB (10756104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2a77e348854277d45c1e9fde2c865dc7df563ac1b4b8cf37804f178aac8d0e`  
		Last Modified: Fri, 18 Mar 2022 05:13:55 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c23c17b302d2d05238335a3dc20c329beff52c9ad26f50d48c661a9edabd5`  
		Last Modified: Fri, 18 Mar 2022 05:13:58 GMT  
		Size: 10.2 MB (10155136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968fccfe45f934832564f41a299fe043f2e3154694e46584b8952dfbc8c79d78`  
		Last Modified: Fri, 18 Mar 2022 05:13:55 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42052840234c254f164e4ba7a6c2242c43a33a8446b93cc9d07f6e71bc2b4b0`  
		Last Modified: Fri, 18 Mar 2022 05:13:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c90f0b65006599e78d5047d7a0bc243a1cbe050388ee1536119c3449c0ed8`  
		Last Modified: Fri, 18 Mar 2022 05:13:55 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e492b533742bd8cbc8e6d1a2d27a16873522a1e9ed4a43b46193f35331c018`  
		Last Modified: Sat, 19 Mar 2022 15:50:20 GMT  
		Size: 1.9 MB (1899699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdd46c086b74f6bb19c09a1035bee8a8049cb804b3a811d88ad1dc140ed5619`  
		Last Modified: Sat, 19 Mar 2022 15:50:20 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9cd318c59aba33e48fb4ff536efa62eec65b7633c00ba00baa722a58034752`  
		Last Modified: Sat, 19 Mar 2022 15:50:20 GMT  
		Size: 575.7 KB (575715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f12ff22ab18b21cb0a442a45a16ab475385415fb12bda04277c296a6e679336`  
		Last Modified: Tue, 22 Mar 2022 22:39:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2da3c34fb7996ed0645f235d4dcaaf7e73873c6a4df664db7c757879ab7b091`  
		Last Modified: Tue, 22 Mar 2022 22:39:41 GMT  
		Size: 20.9 MB (20937827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php7.4-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d61eefdc75f7379ee3a91a17c30d45c60f15f57d06a5fc82c25b4f14b3049938
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142695647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd426270d3aa4fb0d078c580e3c4f5d2e80a158c1964a2db91f5c78f9fa368d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:40 GMT
ADD file:8d54e000817531229c35a32eee074105c7b4d3c08b7ca56b1abdd80571687f28 in / 
# Tue, 29 Mar 2022 02:19:41 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:10:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 29 Mar 2022 07:10:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 29 Mar 2022 07:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:11:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 29 Mar 2022 07:11:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 29 Mar 2022 07:16:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 29 Mar 2022 07:16:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 29 Mar 2022 07:16:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 29 Mar 2022 07:16:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 29 Mar 2022 07:16:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 29 Mar 2022 07:16:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 07:16:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 29 Mar 2022 07:16:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 29 Mar 2022 09:13:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 29 Mar 2022 09:13:27 GMT
ENV PHP_VERSION=7.4.28
# Tue, 29 Mar 2022 09:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Tue, 29 Mar 2022 09:13:28 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Tue, 29 Mar 2022 09:13:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 29 Mar 2022 09:13:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 29 Mar 2022 09:20:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 29 Mar 2022 09:20:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 29 Mar 2022 09:20:36 GMT
RUN docker-php-ext-enable sodium
# Tue, 29 Mar 2022 09:20:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 29 Mar 2022 09:20:37 GMT
STOPSIGNAL SIGWINCH
# Tue, 29 Mar 2022 09:20:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 29 Mar 2022 09:20:40 GMT
WORKDIR /var/www/html
# Tue, 29 Mar 2022 09:20:40 GMT
EXPOSE 80
# Tue, 29 Mar 2022 09:20:41 GMT
CMD ["apache2-foreground"]
# Tue, 29 Mar 2022 11:46:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 11:46:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 29 Mar 2022 11:46:54 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Tue, 29 Mar 2022 11:46:54 GMT
ENV DRUPAL_VERSION=9.3.9
# Tue, 29 Mar 2022 11:46:54 GMT
WORKDIR /opt/drupal
# Tue, 29 Mar 2022 11:47:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 29 Mar 2022 11:47:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d4bf0b27c669e589de33695047d638174fc2ca819a4366d5f80d1ad6b01c0c0e`  
		Last Modified: Tue, 29 Mar 2022 02:35:26 GMT  
		Size: 22.8 MB (22753045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f556041af6c4895a5a79a108ad426f4acd68eccc9bbf408e99eeb772ff938b`  
		Last Modified: Tue, 29 Mar 2022 10:33:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143ea667d8c453dd32a011a5ffaeec170d3da0c6fba06e88fbb9cdf2af5f10f3`  
		Last Modified: Tue, 29 Mar 2022 10:33:50 GMT  
		Size: 59.5 MB (59537662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5765fdaa2e37d313b63de452eb17cd046fd31ad02071583cabd29fc756235d24`  
		Last Modified: Tue, 29 Mar 2022 10:33:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b1927e68778c5beb6d84d5877aeaec3433799a0bcd26b386abb63653da8e0`  
		Last Modified: Tue, 29 Mar 2022 10:34:39 GMT  
		Size: 17.5 MB (17479699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0cce00c9e161592ca1c0b01c5c324c83f28e74644cedb885dcd9f123218380`  
		Last Modified: Tue, 29 Mar 2022 10:34:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5aa384d32114d7c63c8d48ec93877f44d1b64ddfd8dd70010af49afccef9e`  
		Last Modified: Tue, 29 Mar 2022 10:34:32 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549f069f797faea10904dcdafcdc50d96d739ac50211aa9d6b56a4422727a174`  
		Last Modified: Tue, 29 Mar 2022 10:48:52 GMT  
		Size: 10.8 MB (10754217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecd1b97dff29ecea7aaf51956cde8e598acf20011a5540ab70bdc6cb9dc5c29`  
		Last Modified: Tue, 29 Mar 2022 10:48:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b3e0edeb63742c5d36629ff4a68909e5152a7dcbf569c01e298cf33fe4a6cc`  
		Last Modified: Tue, 29 Mar 2022 10:48:52 GMT  
		Size: 9.0 MB (9035626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04725efd47defee4f68413d11b09c3042844346c5f8831300b6b7b0549d7fac`  
		Last Modified: Tue, 29 Mar 2022 10:48:48 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1624b08a80e0630eb1ed5119bad4ff9515ec5b619e0b23ed5adfa2cbf9ee9546`  
		Last Modified: Tue, 29 Mar 2022 10:48:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85728d27c6698094da4ed4a2a5a638015e6738722bad0b344c28e29259a74527`  
		Last Modified: Tue, 29 Mar 2022 10:48:48 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39087cf9c564c71ae76343312d9340fcb51f04f7aa5e648e5f55c6cf6bc36cff`  
		Last Modified: Tue, 29 Mar 2022 14:20:26 GMT  
		Size: 1.6 MB (1615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1c22bae53ef26eb8110c5f0dd8423959e4e901526116a9ca26a53c53518e34`  
		Last Modified: Tue, 29 Mar 2022 14:20:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c1a2da7240437410855210ffc58bb236a92c98318ce3e3e71ec05ec9649d67`  
		Last Modified: Tue, 29 Mar 2022 14:20:26 GMT  
		Size: 575.7 KB (575719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0956fee0f1ce54f7967ac3895dab803ff1213e128fc28ac305a73c4bb16ca02`  
		Last Modified: Tue, 29 Mar 2022 14:20:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2f81f1bd864ecb0c5e9c71581c25d3678a391c13910584e33e87d9398d298f`  
		Last Modified: Tue, 29 Mar 2022 14:20:54 GMT  
		Size: 20.9 MB (20937829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php7.4-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:8987fff6307d89570c3344353d49314e40ba593a8e851a5080c4ace7d4e296fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158343291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23240a18c82356c14fc4dd86c9cbd22858ecd81f3e37cc02c40ede3bd3eaff97`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 14:23:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Mar 2022 14:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Mar 2022 14:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 14:24:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Mar 2022 14:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Mar 2022 14:29:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Mar 2022 14:29:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Mar 2022 14:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Mar 2022 14:29:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Mar 2022 14:29:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Mar 2022 14:29:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 14:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 14:29:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Mar 2022 17:09:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 17 Mar 2022 17:09:46 GMT
ENV PHP_VERSION=7.4.28
# Thu, 17 Mar 2022 17:09:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Thu, 17 Mar 2022 17:09:48 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Thu, 17 Mar 2022 17:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Mar 2022 17:10:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Mar 2022 17:12:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Mar 2022 17:12:18 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Thu, 17 Mar 2022 17:12:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Mar 2022 17:12:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Mar 2022 17:12:20 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Mar 2022 17:12:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Mar 2022 17:12:22 GMT
WORKDIR /var/www/html
# Thu, 17 Mar 2022 17:12:23 GMT
EXPOSE 80
# Thu, 17 Mar 2022 17:12:24 GMT
CMD ["apache2-foreground"]
# Fri, 18 Mar 2022 10:50:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 10:50:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 18 Mar 2022 10:50:26 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Thu, 24 Mar 2022 01:07:02 GMT
ENV DRUPAL_VERSION=9.3.9
# Thu, 24 Mar 2022 01:07:03 GMT
WORKDIR /opt/drupal
# Thu, 24 Mar 2022 01:07:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 24 Mar 2022 01:07:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b6c2b1e25add7315508df3aedb73d3d05b44920510c571e9746aecc9212808`  
		Last Modified: Thu, 17 Mar 2022 18:15:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e868294ede19eddb4934c00c242c3b7fb276b81ef1b28e07cacbda2706c1ad`  
		Last Modified: Thu, 17 Mar 2022 18:15:45 GMT  
		Size: 70.4 MB (70359368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21cecb898c34df71bbb62a78234d013af6c31c04b6d6bf2bcf0c9cf1069d2fc`  
		Last Modified: Thu, 17 Mar 2022 18:15:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7dc7a0d2c7c7d1d85e505ab920ac92bac4ee86551e940ebf88521342e26613`  
		Last Modified: Thu, 17 Mar 2022 18:16:10 GMT  
		Size: 18.4 MB (18367359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102fc95735c5442daa329317212569c18ced614a911e1f610f0c26d76af43d91`  
		Last Modified: Thu, 17 Mar 2022 18:16:07 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6ac8701c91de368e0b9e76f1e6c7d6e8924b623aaba0a9b4b1933295eae930`  
		Last Modified: Thu, 17 Mar 2022 18:16:07 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293bbbb2c4ebfa18e537c7c78e194db4de12368d6b3d69cc7af8bab1eeed53e8`  
		Last Modified: Thu, 17 Mar 2022 18:35:23 GMT  
		Size: 10.5 MB (10542312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1fd19eec91ce83e06e8d9a918bb8cbe302b93bb6c8adf36fa3c69e197cbab5`  
		Last Modified: Thu, 17 Mar 2022 18:35:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e626be36ef51abfad90b3d82a783e4731cefbbfa3b11fd8bec7baef0339db73e`  
		Last Modified: Thu, 17 Mar 2022 18:35:21 GMT  
		Size: 10.0 MB (9962400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7a3d1cb0081b838c2bcf6e5735501ca2b6bd66eff796bc7ce5d73af543c4b0`  
		Last Modified: Thu, 17 Mar 2022 18:35:19 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e252c09245e019a3756d9b1feab1cbb6132ceb393761543e6f983df1c0dfc`  
		Last Modified: Thu, 17 Mar 2022 18:35:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa2415f7eef095266541af3d68f441b54d637f7dd3a9211f5a00a464a7da7c8`  
		Last Modified: Thu, 17 Mar 2022 18:35:19 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf49d849695183c4c11cd1f6895e8885c5ef7b1407e21bb3cfe2ec93ba2478b`  
		Last Modified: Fri, 18 Mar 2022 11:17:07 GMT  
		Size: 1.7 MB (1668645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587b0070f579fa21951af3a2847f8cc36275ecdba4de839cd7588cdf6db1a602`  
		Last Modified: Fri, 18 Mar 2022 11:17:06 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290c41b5a3c5301971be027e37f88455826b33055fbb23e2bec8401b1473a816`  
		Last Modified: Fri, 18 Mar 2022 11:17:06 GMT  
		Size: 575.7 KB (575714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d537f49151e56a33e7ebf37c0f7ff4a5424c9f5f95f8b3c6c2a6cddb6fc853f8`  
		Last Modified: Thu, 24 Mar 2022 01:47:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7025adc4158a736e5a20bb0698665642a5565fc251fb6881f4abeffb82151185`  
		Last Modified: Thu, 24 Mar 2022 01:47:09 GMT  
		Size: 20.9 MB (20938511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php7.4-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:b88cd106bc96a2cfb7d8e9af61ec6c19aef95f6c6f319f0adf4bd32cd5b58e67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172167501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f553497b50fe2359ed5e4ef5e6fca20b074e4c45a075d81744b8513295ece1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Mar 2022 08:16:28 GMT
ADD file:39b40ec7bd2f4e691b74f0287e43ab64ef32f99953e606d9e4b72d058659209c in / 
# Thu, 17 Mar 2022 08:16:29 GMT
CMD ["bash"]
# Wed, 23 Mar 2022 19:48:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 23 Mar 2022 19:48:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 23 Mar 2022 19:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Mar 2022 19:49:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Mar 2022 19:49:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Mar 2022 19:52:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 23 Mar 2022 19:52:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 23 Mar 2022 19:52:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 23 Mar 2022 19:52:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 23 Mar 2022 19:52:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 23 Mar 2022 19:52:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Mar 2022 19:52:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Mar 2022 19:52:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Mar 2022 21:06:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 23 Mar 2022 21:06:43 GMT
ENV PHP_VERSION=7.4.28
# Wed, 23 Mar 2022 21:06:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Wed, 23 Mar 2022 21:06:45 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Wed, 23 Mar 2022 21:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 23 Mar 2022 21:06:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 23 Mar 2022 21:08:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 23 Mar 2022 21:08:39 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Wed, 23 Mar 2022 21:08:39 GMT
RUN docker-php-ext-enable sodium
# Wed, 23 Mar 2022 21:08:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 23 Mar 2022 21:08:41 GMT
STOPSIGNAL SIGWINCH
# Wed, 23 Mar 2022 21:08:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 23 Mar 2022 21:08:43 GMT
WORKDIR /var/www/html
# Wed, 23 Mar 2022 21:08:44 GMT
EXPOSE 80
# Wed, 23 Mar 2022 21:08:45 GMT
CMD ["apache2-foreground"]
# Thu, 24 Mar 2022 07:16:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 24 Mar 2022 07:16:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 24 Mar 2022 07:16:17 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Thu, 24 Mar 2022 07:16:17 GMT
ENV DRUPAL_VERSION=9.3.9
# Thu, 24 Mar 2022 07:16:18 GMT
WORKDIR /opt/drupal
# Thu, 24 Mar 2022 07:16:30 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 24 Mar 2022 07:16:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cef703cf0f3e19a7a5f8b305254c02563c8b07f5b842bb99741d3a2fd136e9f0`  
		Last Modified: Thu, 17 Mar 2022 08:24:59 GMT  
		Size: 27.8 MB (27804570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6261bc527e93258337a0df8e3227a57b50870455eac1496e062bbaa665ad240`  
		Last Modified: Wed, 23 Mar 2022 21:43:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca518d728f4fbc349fae02b5a08389384396ad9361841eb3abf45ab5b2e157`  
		Last Modified: Wed, 23 Mar 2022 21:43:19 GMT  
		Size: 81.2 MB (81229619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e0740016e62d41fb9ad69d15fd3fdcaf989d08771e97c2a75b5700284fbb4a`  
		Last Modified: Wed, 23 Mar 2022 21:43:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb0a247efa5e81993cb47ef8a797eea7fe25c716dfb5fec23d2e999daee9`  
		Last Modified: Wed, 23 Mar 2022 21:43:55 GMT  
		Size: 18.9 MB (18900001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9168a92f0f4dfef71ea314056ad7e49fcdb05099777384ded828e6670fb0c619`  
		Last Modified: Wed, 23 Mar 2022 21:43:52 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7febf828de49c505297f22f5462266ff2acf9dfef6c03ddbccfc96b44f9cb19`  
		Last Modified: Wed, 23 Mar 2022 21:43:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38cfbcf1e6da4aca8e92667c63f9f6e6529cfcb2dfd6519e4dd65f5c9df3dae`  
		Last Modified: Wed, 23 Mar 2022 21:55:33 GMT  
		Size: 10.5 MB (10542932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2266e2491f7db730bfa3d65b6a2e87777c7d803fa62f8731aa669bcc1b972cec`  
		Last Modified: Wed, 23 Mar 2022 21:55:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ba65911f60afce2345b18c52d33b5349b6dd0282b1f9489a34508d679c8d5d`  
		Last Modified: Wed, 23 Mar 2022 21:55:31 GMT  
		Size: 10.4 MB (10390948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac29a50635eae7c71c55141b5b51ceafe0909e1a41a51671e1c05bcf0e80429`  
		Last Modified: Wed, 23 Mar 2022 21:55:29 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c3e45f415e1b00e515b7ff6de1b937a54ba3bff262b967fb460ec64a25a2ae`  
		Last Modified: Wed, 23 Mar 2022 21:55:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6102e2615b8b1f4d8163b8f4d38c6f9bf669eb46759fe4b88a2974b4d5df931`  
		Last Modified: Wed, 23 Mar 2022 21:55:29 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a130d35092e088f0c5430a08489bc03a7f8298c164963af26f848f366a3ccaf5`  
		Last Modified: Thu, 24 Mar 2022 09:23:23 GMT  
		Size: 1.8 MB (1779493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a964dadeecc973c69e93c8ec2bbdd4de5319233f1a84c16970b230084b7bb2d4`  
		Last Modified: Thu, 24 Mar 2022 09:23:22 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5712d5afeb6fa14666d7bd4666e49d2f3f1f264d2ad4003fd76379a2fec9bc`  
		Last Modified: Thu, 24 Mar 2022 09:23:23 GMT  
		Size: 575.7 KB (575711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5bfba98b74d40f8b0633dade8e1d0cf87a3040542ac9568484ab7e04b9f13e`  
		Last Modified: Thu, 24 Mar 2022 09:23:22 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b988f01151a4d68d243cc8330bcc90fc123b9537b196b64700a490aa55630`  
		Last Modified: Thu, 24 Mar 2022 09:23:28 GMT  
		Size: 20.9 MB (20938475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php7.4-apache-buster` - linux; ppc64le

```console
$ docker pull drupal@sha256:368e7fe0a3342d63fdc0d9ee7c42a25c86d68d77060a643071c99a3da432b437
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177908689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abf5f9c3b93e3f32424bfeee4fb8c5aa8c1d3c0ab7822214802ece50a460724`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Mar 2022 11:19:08 GMT
ADD file:0af430b7759619d4d40ea316f823599879e4f3e0dfc8877bdee731020fb2620d in / 
# Thu, 17 Mar 2022 11:19:12 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 13:05:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 18 Mar 2022 13:06:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 18 Mar 2022 13:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 13:09:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Mar 2022 13:10:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 18 Mar 2022 13:21:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 18 Mar 2022 13:21:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 18 Mar 2022 13:23:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 18 Mar 2022 13:24:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 18 Mar 2022 13:24:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 18 Mar 2022 13:24:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Mar 2022 13:24:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Mar 2022 13:25:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Mar 2022 16:35:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 18 Mar 2022 16:35:40 GMT
ENV PHP_VERSION=7.4.28
# Fri, 18 Mar 2022 16:35:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Fri, 18 Mar 2022 16:35:53 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Fri, 18 Mar 2022 16:38:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 18 Mar 2022 16:38:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 18 Mar 2022 16:43:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 18 Mar 2022 16:43:50 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Fri, 18 Mar 2022 16:43:58 GMT
RUN docker-php-ext-enable sodium
# Fri, 18 Mar 2022 16:44:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Mar 2022 16:44:05 GMT
STOPSIGNAL SIGWINCH
# Fri, 18 Mar 2022 16:44:07 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 18 Mar 2022 16:44:10 GMT
WORKDIR /var/www/html
# Fri, 18 Mar 2022 16:44:13 GMT
EXPOSE 80
# Fri, 18 Mar 2022 16:44:16 GMT
CMD ["apache2-foreground"]
# Sat, 19 Mar 2022 22:13:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:13:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 19 Mar 2022 22:13:31 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Tue, 22 Mar 2022 22:38:10 GMT
ENV DRUPAL_VERSION=9.3.9
# Tue, 22 Mar 2022 22:38:13 GMT
WORKDIR /opt/drupal
# Tue, 22 Mar 2022 22:38:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 22 Mar 2022 22:39:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:303d92340e7868a8dc0fdad5d6c67a8a819a74a2bc47038b26339d5be6084bf4`  
		Last Modified: Thu, 17 Mar 2022 11:29:21 GMT  
		Size: 30.6 MB (30562350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95837e03838c8ae24a52d68c38795b37884473b490ea69bc17eafa636b3ba1c9`  
		Last Modified: Fri, 18 Mar 2022 19:08:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87fad4279e4b974d5841af7d823d8e2a8efb34882796087c5921f518b60b4bd`  
		Last Modified: Fri, 18 Mar 2022 19:09:30 GMT  
		Size: 82.3 MB (82292018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b519ad0f798f7ad177060f97cc0a7c3ea13a0f1b9f69fe6f1010362f1cfe0ffc`  
		Last Modified: Fri, 18 Mar 2022 19:08:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16506baba4d6bc6441f111b3e31b5b4c21ee01074d090d44a1b9f137535d2ab2`  
		Last Modified: Fri, 18 Mar 2022 19:10:22 GMT  
		Size: 19.8 MB (19822377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949209f454014e2ebd6840becffbf3902d266bbd1e7c4e32ab46ad8ef6e378d9`  
		Last Modified: Fri, 18 Mar 2022 19:10:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f228ea7940d9b23508de874041860a1b29d79a1e6513c5aac1d4a412d0d5a66`  
		Last Modified: Fri, 18 Mar 2022 19:10:11 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534f5a4fb469750c167d0b3392e1a4d989accb66c6f16132f9e7a7dc91ccb22a`  
		Last Modified: Fri, 18 Mar 2022 19:24:56 GMT  
		Size: 10.8 MB (10756084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b9973ca55353777d6869dc9b33a564d0b01412f8f5c9173e99f4c3080978ef`  
		Last Modified: Fri, 18 Mar 2022 19:24:52 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca1ab9582c2a464cfa577773a99920722d433e228600776f490f8c4118e27ac`  
		Last Modified: Fri, 18 Mar 2022 19:24:54 GMT  
		Size: 10.8 MB (10828124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808ecf79dcab876b6e1bf1b975218adf72ad6e392f3b9710793b42c477a95119`  
		Last Modified: Fri, 18 Mar 2022 19:24:52 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf7591de7e611a3e86559e0bb65702e79e9fc7f56ba19c8698d1a19ba5a5d58`  
		Last Modified: Fri, 18 Mar 2022 19:24:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38318dc20071194bf0ef7392811065084b671a8caef9317be162628c3b008589`  
		Last Modified: Fri, 18 Mar 2022 19:24:52 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82a3397e3fe55627f50c916e0df45d7dc9e44a1c2fafb34c17d345faddb7b01`  
		Last Modified: Sat, 19 Mar 2022 23:14:47 GMT  
		Size: 2.1 MB (2128149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4552f828bd24342f870d0178365be3391a6668b0e08067e0fe3504d9d0ca6b45`  
		Last Modified: Sat, 19 Mar 2022 23:14:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a78ec1241b83ad0d2261e98774a6dc70540a67cc722ff496c38981527fe5a5`  
		Last Modified: Sat, 19 Mar 2022 23:14:46 GMT  
		Size: 575.7 KB (575719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ab149f9ec825971144bcf8a0475c4e45585b1bea39c8757572c01872471393`  
		Last Modified: Tue, 22 Mar 2022 23:25:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1409eaf027c8fc4b7e5a96e8181e26d63a8602b4ec13bcd8f0207a444dc84`  
		Last Modified: Tue, 22 Mar 2022 23:26:28 GMT  
		Size: 20.9 MB (20937949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php7.4-apache-buster` - linux; s390x

```console
$ docker pull drupal@sha256:ab6c9507454b3ecc36f1c9b1652cbb859cdf02bbf6bfba0cb94d9a3b4d35391b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152748236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439d39594e4a75a1af2db858b960fbcc16d197f8417a13dcd60975629832460c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:30 GMT
ADD file:4342e1d9db757e91953273ac7120c9d6004d38281f9cea830898b4f35ca43517 in / 
# Thu, 17 Mar 2022 03:07:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:08:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Mar 2022 09:08:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Mar 2022 09:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 09:08:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Mar 2022 09:08:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Mar 2022 09:12:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Mar 2022 09:12:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Mar 2022 09:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Mar 2022 09:12:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Mar 2022 09:12:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Mar 2022 09:12:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 09:12:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 09:12:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Mar 2022 11:01:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 17 Mar 2022 11:01:41 GMT
ENV PHP_VERSION=7.4.28
# Thu, 17 Mar 2022 11:01:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.28.tar.xz.asc
# Thu, 17 Mar 2022 11:01:41 GMT
ENV PHP_SHA256=9cc3b6f6217b60582f78566b3814532c4b71d517876c25013ae51811e65d8fce
# Thu, 17 Mar 2022 11:01:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Mar 2022 11:01:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Mar 2022 11:03:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Mar 2022 11:03:22 GMT
COPY multi:ee8b9bb4e448c5d38508b40a8ace77d14cf000229390e687b6d467283c9826e6 in /usr/local/bin/ 
# Thu, 17 Mar 2022 11:03:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Mar 2022 11:03:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Mar 2022 11:03:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Mar 2022 11:03:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Mar 2022 11:03:23 GMT
WORKDIR /var/www/html
# Thu, 17 Mar 2022 11:03:23 GMT
EXPOSE 80
# Thu, 17 Mar 2022 11:03:23 GMT
CMD ["apache2-foreground"]
# Thu, 17 Mar 2022 21:19:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:19:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Mar 2022 21:19:27 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Tue, 22 Mar 2022 21:51:33 GMT
ENV DRUPAL_VERSION=9.3.9
# Tue, 22 Mar 2022 21:51:33 GMT
WORKDIR /opt/drupal
# Tue, 22 Mar 2022 21:51:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 22 Mar 2022 21:51:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6f8a08956872b0f67802da3a67e007322eb963a60e0dadd736077f3ece414e1f`  
		Last Modified: Thu, 17 Mar 2022 03:13:18 GMT  
		Size: 25.8 MB (25769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc72acd2dc6ea4ea7e921a154c127beeb2bbe65bb77a3770e49e4f7a5d38d51`  
		Last Modified: Thu, 17 Mar 2022 11:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c130d936c6d923444315825d6c86136e0f51e13f08d9159fad3d8c3fbddef678`  
		Last Modified: Thu, 17 Mar 2022 11:56:12 GMT  
		Size: 64.7 MB (64712322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0c874059d92bfeaa8d5758b9fc43758f30edfea4543ad5c67b4230f2fea34c`  
		Last Modified: Thu, 17 Mar 2022 11:56:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9127d796169297a0dadf84fc01a05d55751366153cd11aab39a808657c1409f5`  
		Last Modified: Thu, 17 Mar 2022 11:56:29 GMT  
		Size: 18.5 MB (18524779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219552ffb21795d6aa14fae34ec51d64803bde1234ec1049f82b03617654dd6d`  
		Last Modified: Thu, 17 Mar 2022 11:56:26 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37120a00b85d2dd8881f86c8b9943ae4ade24174c42004464acf06775172dd2`  
		Last Modified: Thu, 17 Mar 2022 11:56:26 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6daff11bbcf01e0b246f975ad771c364d6dad8388d0ea4e59340c839b04ba1`  
		Last Modified: Thu, 17 Mar 2022 12:08:28 GMT  
		Size: 10.8 MB (10754563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d91448085b05e12126ba8db947f02908f2c3951f5ec0b62aabff5c2d0c51b0e`  
		Last Modified: Thu, 17 Mar 2022 12:08:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ead7ace830245b0f6d824c0512ad464241c1bc3761f019b2493c07df9ce58a`  
		Last Modified: Thu, 17 Mar 2022 12:08:27 GMT  
		Size: 9.6 MB (9624861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce3199786f17a4283346831a408316817b54ac9e8f664058d83b5f90a48de6`  
		Last Modified: Thu, 17 Mar 2022 12:08:26 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75c459e8f873873d5448ad3e6964e3bd148a548fbe38d4f59b21f6ff2e33ba0`  
		Last Modified: Thu, 17 Mar 2022 12:08:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00d772c2c72fa31571c949c2a22cdb76dda00baa3287a6633826a266e27e734`  
		Last Modified: Thu, 17 Mar 2022 12:08:26 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d347961cc85dbc3003cf904a7781051432639ddf57e93543edbf102cd964382`  
		Last Modified: Thu, 17 Mar 2022 21:41:01 GMT  
		Size: 1.8 MB (1843235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cfa546e4f995a416306000e3e4ce7fda0609bbf1404bd4abb93adf32839937`  
		Last Modified: Thu, 17 Mar 2022 21:41:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11a6ccde1ae821bfeecb76bf2dc1d91d9be8097a3252a01cfba8ac499de9292`  
		Last Modified: Thu, 17 Mar 2022 21:41:01 GMT  
		Size: 575.7 KB (575712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd966690ecffe097fe940bdea7bd0767fe6477526644736cc849a54acbbc836`  
		Last Modified: Tue, 22 Mar 2022 22:12:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9538282dc2f7c49f11914253572779976d9e939b77948e37e463ba4781fbc27`  
		Last Modified: Tue, 22 Mar 2022 22:12:48 GMT  
		Size: 20.9 MB (20937788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
