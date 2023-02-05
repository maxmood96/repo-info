## `drupal:9-apache-buster`

```console
$ docker pull drupal@sha256:6e6afc72976744ead306b203a0817955c1955b9250f0d10437b416ec1b42cd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:9-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:09928f0645fee3453c238c13ac85b56f2813732bbc86ee2251ed648bd92c0786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171312966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc2391bef851e29e7d861cfab3423f373bd8d26e80cb5d765a5916701358b00`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 18:47:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 18:47:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 18:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 18:48:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 18:48:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 18:51:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 04 Feb 2023 18:51:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 04 Feb 2023 18:51:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 04 Feb 2023 18:51:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 04 Feb 2023 18:51:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 04 Feb 2023 18:51:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 18:51:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 18:51:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 19:18:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 04 Feb 2023 19:18:13 GMT
ENV PHP_VERSION=8.1.15
# Sat, 04 Feb 2023 19:18:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.15.tar.xz.asc
# Sat, 04 Feb 2023 19:18:13 GMT
ENV PHP_SHA256=cd450fb4ee50488c5bf5f08851f514e5a1cac18c9512234d9e16c3a1d35781a6
# Sat, 04 Feb 2023 19:18:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 19:18:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 19:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 19:21:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 04 Feb 2023 19:21:27 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 19:21:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 19:21:27 GMT
STOPSIGNAL SIGWINCH
# Sat, 04 Feb 2023 19:21:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 04 Feb 2023 19:21:27 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 19:21:27 GMT
EXPOSE 80
# Sat, 04 Feb 2023 19:21:27 GMT
CMD ["apache2-foreground"]
# Sun, 05 Feb 2023 02:32:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 05 Feb 2023 02:32:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 05 Feb 2023 02:32:47 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sun, 05 Feb 2023 02:34:53 GMT
ENV DRUPAL_VERSION=9.5.3
# Sun, 05 Feb 2023 02:34:53 GMT
WORKDIR /opt/drupal
# Sun, 05 Feb 2023 02:35:04 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sun, 05 Feb 2023 02:35:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae08958ff1bd1856a03e2bfbae52b79c27be0d2f80bf155c8aa532f9ad46e220`  
		Last Modified: Sat, 04 Feb 2023 19:58:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db284214e0a94216b2a47f1bf6f9a9adf6209c7b73a59ea110027e2cb6e54469`  
		Last Modified: Sat, 04 Feb 2023 19:59:01 GMT  
		Size: 76.7 MB (76688297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881a1d9f7f864087aced46e16f6fb5f479692c06e9f75bc2b4b6f6af074a402d`  
		Last Modified: Sat, 04 Feb 2023 19:58:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551e93fcc836c645a28465dff51ca167571c0c7b2e51f53535a02b1f149e919c`  
		Last Modified: Sat, 04 Feb 2023 19:59:28 GMT  
		Size: 18.7 MB (18684933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2017a467471efaf04f51e06eb64ed8a4b6d76011d05fe8cd900d7b839a6f312c`  
		Last Modified: Sat, 04 Feb 2023 19:59:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd67da303719005dd7a8fc168c7c4e784f749d3099aa9b18d1dd3ca63d61cd8`  
		Last Modified: Sat, 04 Feb 2023 19:59:25 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1824d9420c37ebb0ebe3d2d3b04adc680234711c541c9d668b6364c38a9030e7`  
		Last Modified: Sat, 04 Feb 2023 20:02:17 GMT  
		Size: 12.2 MB (12153254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de8d7b8a51f4c871fb9f3dbaa6ca6545edeeeb9194b20f377e5e8a48c553a33`  
		Last Modified: Sat, 04 Feb 2023 20:02:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2490cc92bcc86182c07fee78b56297fab189b4190b77e4b8d6f34d7650caff`  
		Last Modified: Sat, 04 Feb 2023 20:02:16 GMT  
		Size: 11.0 MB (11007252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d883e65b803629c94444398f9e7f3cf3b79af6b3158651477510ceebecde1fed`  
		Last Modified: Sat, 04 Feb 2023 20:02:14 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dcd2bc86fb684118ccbe99ea5985ea1d92ef15257e2d39fadf3d39f06c58ad`  
		Last Modified: Sat, 04 Feb 2023 20:02:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d6a9371e5dfcba57a1837c91580d9fe2b411e6697fde12e36a7fce79f17d86`  
		Last Modified: Sat, 04 Feb 2023 20:02:14 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003d752cae53c6506b114645ff8027b1d760c662924e98e3eb4766d09999662d`  
		Last Modified: Sun, 05 Feb 2023 02:51:23 GMT  
		Size: 2.1 MB (2089096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eb1b16bf3e7a1e32ec0680dc27b5d0a8fd9ae0ea9b439374d1e0c966230151`  
		Last Modified: Sun, 05 Feb 2023 02:51:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e5cfc7362c4d836c5ad2b98586ebbfb86ed14f5774a9af300b80eca555330f`  
		Last Modified: Sun, 05 Feb 2023 02:51:23 GMT  
		Size: 700.1 KB (700097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f2b91246d3739c2905439a16f54d41a5ce9441930ec2975aacc6fe642f487d`  
		Last Modified: Sun, 05 Feb 2023 02:53:40 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0568046c098419d75b239eaf5f3e2edfca6a0990b5611522651e3acda9e611ab`  
		Last Modified: Sun, 05 Feb 2023 02:53:46 GMT  
		Size: 22.8 MB (22843637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2aa5a8fc5c94396f53389e31d007f9eac74838369812c73f8562255bbbf5a36f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b92841ff862e07594cbc3103a4722ef885d35952294d8f85741b179ddb2de3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 04 Feb 2023 10:00:07 GMT
ADD file:846a879e62f9818b9aa015fa10169114de528e64d1a704cdcd1e7ee2b0707dac in / 
# Sat, 04 Feb 2023 10:00:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:45:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 17:45:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 17:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:45:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 17:45:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 17:48:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 04 Feb 2023 17:48:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 04 Feb 2023 17:48:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 04 Feb 2023 17:48:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 04 Feb 2023 17:48:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 04 Feb 2023 17:48:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 17:48:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 17:48:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 18:10:38 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 04 Feb 2023 18:10:38 GMT
ENV PHP_VERSION=8.1.15
# Sat, 04 Feb 2023 18:10:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.15.tar.xz.asc
# Sat, 04 Feb 2023 18:10:38 GMT
ENV PHP_SHA256=cd450fb4ee50488c5bf5f08851f514e5a1cac18c9512234d9e16c3a1d35781a6
# Sat, 04 Feb 2023 18:10:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 18:10:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 18:13:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 18:13:15 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 04 Feb 2023 18:13:16 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 18:13:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 18:13:16 GMT
STOPSIGNAL SIGWINCH
# Sat, 04 Feb 2023 18:13:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 04 Feb 2023 18:13:16 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 18:13:16 GMT
EXPOSE 80
# Sat, 04 Feb 2023 18:13:16 GMT
CMD ["apache2-foreground"]
# Sun, 05 Feb 2023 08:54:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 05 Feb 2023 08:54:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 05 Feb 2023 08:54:23 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sun, 05 Feb 2023 08:57:05 GMT
ENV DRUPAL_VERSION=9.5.3
# Sun, 05 Feb 2023 08:57:05 GMT
WORKDIR /opt/drupal
# Sun, 05 Feb 2023 08:57:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sun, 05 Feb 2023 08:57:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8f31db5a63e959a9d015a334241216fa6923a49f0bc031bde1bf336efc7a9614`  
		Last Modified: Sat, 04 Feb 2023 10:07:17 GMT  
		Size: 22.7 MB (22748916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd9c5e07ad6aabb7f2d5afcd2bd672f5ce044d8d8232c1d426c6ee304bd8089`  
		Last Modified: Sat, 04 Feb 2023 18:52:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376b0a5b355348b427e4584aa60883dc7f2c8028164154ecc5d6a971e08c2b63`  
		Last Modified: Sat, 04 Feb 2023 18:52:15 GMT  
		Size: 59.5 MB (59541437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535c3c3ca3201e7c8dd97d901114d29bfd620670e80e44af5595ad010f61f766`  
		Last Modified: Sat, 04 Feb 2023 18:52:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805381d26ffc289def52fb171e9b3a70eaf703d6ab627c8375f47a20b68079ee`  
		Last Modified: Sat, 04 Feb 2023 18:52:52 GMT  
		Size: 17.5 MB (17481422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f5cfbcbb17f5eb05e00a4ef56fbca1806ee26beeeb8b034b79780c44e7eb70`  
		Last Modified: Sat, 04 Feb 2023 18:52:49 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbf6a55fce16e6f9531c8d3d16f32fac3fe39a6ce139ba3db7122d9d6a246e`  
		Last Modified: Sat, 04 Feb 2023 18:52:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945f2bc73df3b8e592099c43a5ca9468cda9c3e01db28e74007d0d6f5f81d4f7`  
		Last Modified: Sat, 04 Feb 2023 18:56:42 GMT  
		Size: 12.2 MB (12151114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabec90ee37fc1cf91df9d551bcba4c17e64d9d4d051c573f21f759a7fc13faf`  
		Last Modified: Sat, 04 Feb 2023 18:56:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fe2cda68fc18d1e8a3e31e3a4fa8e5b0e916d958e27e9600128c1de3accddf`  
		Last Modified: Sat, 04 Feb 2023 18:56:41 GMT  
		Size: 9.5 MB (9503699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e400b40f72042934999e5810701581a4258355db300223e7171607eabf1f93db`  
		Last Modified: Sat, 04 Feb 2023 18:56:39 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b626973a1fbcb1cf755374947cfe7d410cbdc99a7838923e9f808ab1767b4329`  
		Last Modified: Sat, 04 Feb 2023 18:56:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf37f913a23847667936ded4b0cbfb7438eb9089915edd143f54749c0153bde`  
		Last Modified: Sat, 04 Feb 2023 18:56:39 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624bba5fb48a20840e08bec8f9663f58e68ac261bd6d5907e1ebe9625f3604ec`  
		Last Modified: Sun, 05 Feb 2023 09:25:55 GMT  
		Size: 1.5 MB (1481490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93334e955021b0bbc4a9c9a4648091c01b16b2d08d496da47270e84238980747`  
		Last Modified: Sun, 05 Feb 2023 09:25:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4107dcd1ded05c7f10841eb63e7afb9fbb1a25f3bd3551faa2e252a8e3bd411`  
		Last Modified: Sun, 05 Feb 2023 09:25:55 GMT  
		Size: 700.1 KB (700097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e2df668835788b8077e405e089a465ce485aa6c7b6a0843850c8870917e8d`  
		Last Modified: Sun, 05 Feb 2023 09:29:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46010a94fcbd289bd9805c511d6e8da37e83eab42842589e00edc581a8c15ad7`  
		Last Modified: Sun, 05 Feb 2023 09:29:21 GMT  
		Size: 22.8 MB (22844460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d066d7f716669c4a52ce9a094e2085d2ef7a180eabf342d06149c7e4a73cef4b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164006039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a384a9516309fcadf9624133ca09859f74794736f1f7f3050ab7f0189b007413`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:54 GMT
ADD file:cf6ecb1d6b034b0d4fc309542cb25fff0c997661b323f524ecc258ac323e43f6 in / 
# Sat, 04 Feb 2023 06:17:55 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 12:18:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 12:18:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 12:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 12:19:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 12:19:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 12:22:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 04 Feb 2023 12:22:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 04 Feb 2023 12:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 04 Feb 2023 12:22:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 04 Feb 2023 12:22:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 04 Feb 2023 12:22:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 12:22:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 12:22:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 12:46:49 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 04 Feb 2023 12:46:49 GMT
ENV PHP_VERSION=8.1.15
# Sat, 04 Feb 2023 12:46:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.15.tar.xz.asc
# Sat, 04 Feb 2023 12:46:49 GMT
ENV PHP_SHA256=cd450fb4ee50488c5bf5f08851f514e5a1cac18c9512234d9e16c3a1d35781a6
# Sat, 04 Feb 2023 12:47:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 12:47:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 12:49:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 12:49:45 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 04 Feb 2023 12:49:46 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 12:49:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 12:49:46 GMT
STOPSIGNAL SIGWINCH
# Sat, 04 Feb 2023 12:49:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 04 Feb 2023 12:49:46 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 12:49:46 GMT
EXPOSE 80
# Sat, 04 Feb 2023 12:49:46 GMT
CMD ["apache2-foreground"]
# Sat, 04 Feb 2023 22:15:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 22:15:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 04 Feb 2023 22:15:54 GMT
COPY file:81cad59228e2dc61b9d880277f60e1ab16f4d7a32f9f11b33c68bd0b2bacdc3a in /usr/local/bin/ 
# Sat, 04 Feb 2023 22:18:49 GMT
ENV DRUPAL_VERSION=9.5.3
# Sat, 04 Feb 2023 22:18:50 GMT
WORKDIR /opt/drupal
# Sat, 04 Feb 2023 22:19:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 04 Feb 2023 22:19:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bd2853c1424a5596deda2f31e1f82920613a03c667c3ff58cb461340b7bb89cd`  
		Last Modified: Sat, 04 Feb 2023 06:22:04 GMT  
		Size: 25.9 MB (25922631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78a59b8ccf3c868a96ffe9151ff3a1f1a89fee4d0151785e9080a02e8767c46`  
		Last Modified: Sat, 04 Feb 2023 13:18:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c974607a8d0be8f9cd77efc0f50a9b22ac01baef575c035f7e8f6cef7654dd`  
		Last Modified: Sat, 04 Feb 2023 13:19:00 GMT  
		Size: 70.4 MB (70361880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dae2c40cdca83210ffd87d10080044d2271241f03f6ca418351c27703acbeb`  
		Last Modified: Sat, 04 Feb 2023 13:18:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8f0075a627a6b12b30298d5bf854f7411c7d68dae15b528a6f6d3b1fd8080c`  
		Last Modified: Sat, 04 Feb 2023 13:19:26 GMT  
		Size: 18.6 MB (18583775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6296bd37059766b25cf9b0897f32e61829223f7fd097c50663fde2c2751791d`  
		Last Modified: Sat, 04 Feb 2023 13:19:24 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32f1050e799c5b0f54255f9f7bd7821dbe7aeaf9935773004050383fc15b0c7`  
		Last Modified: Sat, 04 Feb 2023 13:19:24 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240e1e7fc6740aefe46c9e0bdfbc1c3810c95245c3e4dc1d1b16976cf0a8fe89`  
		Last Modified: Sat, 04 Feb 2023 13:22:10 GMT  
		Size: 12.2 MB (12151876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e436fe830ef33be30aaf1e4c878e4ef11fa4a681b624b77717ea643017d1bd`  
		Last Modified: Sat, 04 Feb 2023 13:22:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9400b239a83a3a25adc65cd1c1c1534f248d220294378be2fbf0c2acadd293`  
		Last Modified: Sat, 04 Feb 2023 13:22:09 GMT  
		Size: 11.1 MB (11078857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106db91ed3e17d68628dd0d903519efa60b027f1921cd4f90c7df713dd5785a`  
		Last Modified: Sat, 04 Feb 2023 13:22:07 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bd31c19fc31441d34ecb98a08f6e20908a4af23b572510a235191082d0fc0e`  
		Last Modified: Sat, 04 Feb 2023 13:22:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d653fcabcf49f8f3b58aa4264f2381a4848f09c685294cd01209a249f443b5f9`  
		Last Modified: Sat, 04 Feb 2023 13:22:07 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab2243f9bf2912ca05b0d65e2d50343fb490437fbf83c64f994e50149fbd06f`  
		Last Modified: Sat, 04 Feb 2023 22:35:34 GMT  
		Size: 2.4 MB (2356589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6d46e661c6e65f1aacdd361f0c10cbda4b30e79f1ae942cf0895991695e410`  
		Last Modified: Sat, 04 Feb 2023 22:35:33 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25780f5ef7acb9c34d20726db003ba6a21eb8ea2a0b6475e40d8a4ed9b74b725`  
		Last Modified: Sat, 04 Feb 2023 22:35:33 GMT  
		Size: 700.1 KB (700097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7641f24b938bca218c49ab6ee09ad9ee0f0d15219a24a4d167dddc9dbf19b`  
		Last Modified: Sat, 04 Feb 2023 22:37:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d99002f166f6461834776b3b085a3a65777257dddfdc85ddc47bf1609afd52`  
		Last Modified: Sat, 04 Feb 2023 22:37:53 GMT  
		Size: 22.8 MB (22844304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:c77ee2de9216d4f07088ab796a94495edbe7ef1cb36948ecc1d4fc217530efe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176592741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece8d11980e2fea7bfc57fc18da526c9d990edcaf0965335410f4a693343558a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:48 GMT
ADD file:060bbacc8df3d1b157ff409535b3ea29dd0b5667425e3dcf6e60556dcfa4e7f1 in / 
# Sat, 04 Feb 2023 07:49:48 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:30:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 04 Feb 2023 14:30:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 04 Feb 2023 14:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:30:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 04 Feb 2023 14:30:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 04 Feb 2023 14:33:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 04 Feb 2023 14:33:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 04 Feb 2023 14:34:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 04 Feb 2023 14:34:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 04 Feb 2023 14:34:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 04 Feb 2023 14:34:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 14:34:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 04 Feb 2023 14:34:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 04 Feb 2023 14:59:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 04 Feb 2023 14:59:22 GMT
ENV PHP_VERSION=8.1.15
# Sat, 04 Feb 2023 14:59:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.15.tar.xz.asc
# Sat, 04 Feb 2023 14:59:24 GMT
ENV PHP_SHA256=cd450fb4ee50488c5bf5f08851f514e5a1cac18c9512234d9e16c3a1d35781a6
# Sat, 04 Feb 2023 14:59:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 04 Feb 2023 14:59:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 04 Feb 2023 15:02:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 04 Feb 2023 15:02:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 04 Feb 2023 15:02:19 GMT
RUN docker-php-ext-enable sodium
# Sat, 04 Feb 2023 15:02:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 04 Feb 2023 15:02:20 GMT
STOPSIGNAL SIGWINCH
# Sat, 04 Feb 2023 15:02:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 04 Feb 2023 15:02:22 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 15:02:23 GMT
EXPOSE 80
# Sat, 04 Feb 2023 15:02:24 GMT
CMD ["apache2-foreground"]
# Sat, 04 Feb 2023 23:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 23:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 04 Feb 2023 23:35:21 GMT
COPY file:e2da1c2113094da76d330eef39e0e1916af11394dff778e02af557c116266d7c in /usr/local/bin/ 
# Sat, 04 Feb 2023 23:37:58 GMT
ENV DRUPAL_VERSION=9.5.3
# Sat, 04 Feb 2023 23:37:58 GMT
WORKDIR /opt/drupal
# Sat, 04 Feb 2023 23:38:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 04 Feb 2023 23:38:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8e0d975bedf8c90406704c677df48435cd2d53449ac9ab15a876323ceb95ff8f`  
		Last Modified: Sat, 04 Feb 2023 07:55:52 GMT  
		Size: 27.8 MB (27798503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7530cf666fff6e57c2fd7b789b76bf7b9512b00c5d78ed4d83019d31c306e105`  
		Last Modified: Sat, 04 Feb 2023 15:42:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdb983fe81a5de6de33350ecbdd92cb52b3afb4f1d1d693c6384470024c6940`  
		Last Modified: Sat, 04 Feb 2023 15:42:51 GMT  
		Size: 81.2 MB (81235952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035ed3a2e1d31e52d608036c5e463521bd61f242d5c91be4dd94cecd412b6d2`  
		Last Modified: Sat, 04 Feb 2023 15:42:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98abcc7f65763b73045c0d8135d34b1cb01fb29e49166288419c274222a2c80`  
		Last Modified: Sat, 04 Feb 2023 15:43:24 GMT  
		Size: 18.9 MB (18900914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e57b192e06f27e9d7c200c20e1993e9c8ebe059f008ec74709b1b399c9435`  
		Last Modified: Sat, 04 Feb 2023 15:43:21 GMT  
		Size: 430.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc2168488272c2b60614ea16b164dfa7a80886809af6f6497eeb098a6a56b9d`  
		Last Modified: Sat, 04 Feb 2023 15:43:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439962b36cb64a01976480bff6b349b9be62feaa17ab2547f33d9b5c839213c3`  
		Last Modified: Sat, 04 Feb 2023 15:46:50 GMT  
		Size: 11.9 MB (11940006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63aced8d278eb3d155a12fa0bc9a542e4f72fb792d3a3eb6547bf0263593eb1c`  
		Last Modified: Sat, 04 Feb 2023 15:46:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8c95dd8dd345318afbd7dbfada083ada687ed4dda5d797fa2466802fb6aa69`  
		Last Modified: Sat, 04 Feb 2023 15:46:49 GMT  
		Size: 11.2 MB (11228397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47972d349c983f0d2e77a2015063760ec22e3c71898a64c9f6b11b2ee71b38d`  
		Last Modified: Sat, 04 Feb 2023 15:46:47 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db68516ea5ee5ec8e7adb01c249c6afee2dd2a2dc75877429bbad606980e540`  
		Last Modified: Sat, 04 Feb 2023 15:46:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4330ffd0b1fd27262f0be8d397e5ef35b6ae945748c37d05c0a73b4011c1e9b1`  
		Last Modified: Sat, 04 Feb 2023 15:46:47 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1625bf750e8b1ed8be3fed62213b23a097350e5bc92fedc4fbd3de52fc70be9`  
		Last Modified: Sun, 05 Feb 2023 00:02:37 GMT  
		Size: 1.9 MB (1944459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbf0ce0ac7d685aeb4068c71cfc3469a729d1d6b68c98aa468d20f915889027`  
		Last Modified: Sun, 05 Feb 2023 00:02:36 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba259ba3e0ffda7a7cdcd3e2434dca83f9cd25d101736b30664c58d1c179370a`  
		Last Modified: Sun, 05 Feb 2023 00:02:37 GMT  
		Size: 695.2 KB (695200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bae7e1b3aed30fb4463a3adda719a5bbc947f27fe5653bc7c9564ac429a746`  
		Last Modified: Sun, 05 Feb 2023 00:05:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6c4d9697b119855a4beb59ad6f3063b2aa5d4307d2d5ed7ccb063e7f75c984`  
		Last Modified: Sun, 05 Feb 2023 00:05:32 GMT  
		Size: 22.8 MB (22843423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
