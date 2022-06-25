## `drupal:7-php8.0-apache-buster`

```console
$ docker pull drupal@sha256:4b29a6555c57b135e494b174690c50e7e802d01a84c25e971690c13b309a1c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `drupal:7-php8.0-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:5877bf0c912e614a593505fefc29418911a89f28131b4eb88464adfeb6398490
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e102634b76dde35a1a1118ce54008e8cd1842972a5caabd570f26d27fe0f0ed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 07:35:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 07:35:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 07:35:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 07:35:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 07:39:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 07:39:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 07:39:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 07:39:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 07:39:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 07:39:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 07:39:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 07:39:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 08:31:35 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 08:31:35 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 08:31:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 08:31:35 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 08:31:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 08:31:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 08:34:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 08:34:40 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 08:34:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 08:34:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 08:34:41 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 08:34:41 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 08:34:41 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 08:34:42 GMT
EXPOSE 80
# Thu, 23 Jun 2022 08:34:42 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jun 2022 00:15:11 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 00:15:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jun 2022 00:23:41 GMT
ENV DRUPAL_VERSION=7.90
# Fri, 24 Jun 2022 00:23:41 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Fri, 24 Jun 2022 00:23:42 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d0f41537a4bb341b83f091698de52574e75c662ac8cb471ab039c882249ba3`  
		Last Modified: Thu, 23 Jun 2022 09:05:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ded8da51ea293b1ab37514236d32967318d3b94f1df347f87d941d0d6e575`  
		Last Modified: Thu, 23 Jun 2022 09:05:45 GMT  
		Size: 76.7 MB (76683783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2ec4360a6f882047371245cbfceb8084bb7a9edf74f3e8953e74dc448c1d7d`  
		Last Modified: Thu, 23 Jun 2022 09:05:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adb62352a49ca6be79e402f6303985b6fbbbb8a4aff2cc29a7c97d7519450e9`  
		Last Modified: Thu, 23 Jun 2022 09:06:05 GMT  
		Size: 18.7 MB (18681636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2f29c450143f6c17e126bbda6f19c477c624d53db75a4e6e4c0c9bf1546fc6`  
		Last Modified: Thu, 23 Jun 2022 09:06:03 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5792816d4a9ee451189eaa7ef87e3d8806a85d4ae617f2e9da6f09770fa32e`  
		Last Modified: Thu, 23 Jun 2022 09:06:03 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568b1b15fee05e45a915658bc54ff3b06081df7146cadd7e8bc8b1cbd1482504`  
		Last Modified: Thu, 23 Jun 2022 09:12:54 GMT  
		Size: 11.2 MB (11216704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a979a9ecefe8e29e81ecbac806a8b51b7d2fd94db3e83d4e5e348ed3ab840e4f`  
		Last Modified: Thu, 23 Jun 2022 09:12:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81adecfecc360b1cad462bb16f3c4666bf8a806d6f9e8271f7d1c9bc1707345f`  
		Last Modified: Thu, 23 Jun 2022 09:12:53 GMT  
		Size: 10.7 MB (10725066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f410be2acb77a63b40399f8c4da066988a167910841dac97dff8f81e7e754c`  
		Last Modified: Thu, 23 Jun 2022 09:12:51 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e14392e2d5a006f01eaafee9bdb6c1bc6bdb840f45c22335bb301275bd39b0`  
		Last Modified: Thu, 23 Jun 2022 09:12:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f9d5323795a19c374f2f5159d6a3cae6a7ec9b1c3f50daa48a2e525c97dce5`  
		Last Modified: Thu, 23 Jun 2022 09:12:51 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918f6c33f1d4d79dff0457c9bb592ae3c010119d35f8e87ff2b95def7611d7d5`  
		Last Modified: Fri, 24 Jun 2022 00:36:54 GMT  
		Size: 2.2 MB (2244436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e798290fc82ff959491dfd653648021304facd0c7b1d621444d3816c203ca415`  
		Last Modified: Fri, 24 Jun 2022 00:36:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b0542576f204679b9897f54bc494d068424f1418d67389e061cb77da21954`  
		Last Modified: Fri, 24 Jun 2022 00:46:20 GMT  
		Size: 3.4 MB (3388626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; arm variant v5

```console
$ docker pull drupal@sha256:943d04428b58175de35b48276765ea91fceb69cf30d239d54ba1f154220595b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127848575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b10e965808623d0cb9bc8da06c4f716a0464395cf52f25ffa92d7d6f094e1b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:39 GMT
ADD file:b1e035d48236f9259b8573f7b0ac432e69c0d8d42292d24b41d94cba3b942eab in / 
# Thu, 23 Jun 2022 00:51:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 23:58:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 23:58:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 23:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 23:59:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 23:59:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Jun 2022 00:05:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jun 2022 00:05:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jun 2022 00:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 24 Jun 2022 00:06:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 24 Jun 2022 00:06:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 24 Jun 2022 00:06:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jun 2022 00:06:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jun 2022 00:06:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jun 2022 02:21:34 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 24 Jun 2022 03:06:06 GMT
ENV PHP_VERSION=8.0.20
# Fri, 24 Jun 2022 03:06:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Fri, 24 Jun 2022 03:06:06 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Fri, 24 Jun 2022 03:06:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jun 2022 03:06:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jun 2022 03:11:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 24 Jun 2022 03:11:46 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 24 Jun 2022 03:11:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jun 2022 03:11:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jun 2022 03:11:49 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jun 2022 03:11:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jun 2022 03:11:50 GMT
WORKDIR /var/www/html
# Fri, 24 Jun 2022 03:11:51 GMT
EXPOSE 80
# Fri, 24 Jun 2022 03:11:51 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jun 2022 13:07:11 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 13:07:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jun 2022 13:07:13 GMT
ENV DRUPAL_VERSION=7.90
# Fri, 24 Jun 2022 13:07:13 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Fri, 24 Jun 2022 13:07:17 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:e6235ec1c9144fd72693df78eccd13b2e35d15fb254f6e0e7dd5ff17a944f0e7`  
		Last Modified: Thu, 23 Jun 2022 01:07:10 GMT  
		Size: 24.9 MB (24889983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97652c4e6f12dbd2a2c7f3c9abd595fa9ebe233136cf3a378e330204b77284c2`  
		Last Modified: Fri, 24 Jun 2022 04:20:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736eca0c5e581ebe05218abdad2a37a7171c31c241acf99e75fde8d3e12bb88e`  
		Last Modified: Fri, 24 Jun 2022 04:21:33 GMT  
		Size: 58.8 MB (58827152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dea73009c526b2f97a0b7aa233a5f52b72fd093354f5874909bbb52feb3c70e`  
		Last Modified: Fri, 24 Jun 2022 04:20:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2f04ce987dbf30b8a74f70e2616b7259b28cca14331a174c3bd03aa87897f7`  
		Last Modified: Fri, 24 Jun 2022 04:22:05 GMT  
		Size: 18.0 MB (18023970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1b5da3964fd314748d87626dfcd3223ff40369c53d23a97311a872f06430e8`  
		Last Modified: Fri, 24 Jun 2022 04:21:54 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473250af51e09752bc54e359fa86331214100b9fb2906141c40ecf3f6e475f00`  
		Last Modified: Fri, 24 Jun 2022 04:21:55 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907f6441dd5970caacbb7423e0cb7e268ec4ae82e335b5e68f7a9ec2f7cc49c`  
		Last Modified: Fri, 24 Jun 2022 04:42:03 GMT  
		Size: 11.2 MB (11214979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b8c3891a4f5cc4fb565f61ec73f5fc15058fffd0f0fc60115967c24c01df43`  
		Last Modified: Fri, 24 Jun 2022 04:41:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce4806507ffa5ad5884e16ec24c3718bd0da60e440940f42f69f9fc1c23986`  
		Last Modified: Fri, 24 Jun 2022 04:42:07 GMT  
		Size: 9.7 MB (9740605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3a4f83d6baf1b6ddf6244ed5404e5dff9756d816217981e8610916cb71c294`  
		Last Modified: Fri, 24 Jun 2022 04:41:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5f80a41f357578085d8c68ed5c0af8ccd659ffc6d7c5bc9b081699d41ba696`  
		Last Modified: Fri, 24 Jun 2022 04:41:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1092266ee8937b1d1a96ccd1e191326798a467defc724e4b3274852d16a8a597`  
		Last Modified: Fri, 24 Jun 2022 04:41:59 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d62843df0509817580bc477dc737ae7121037aa0b1edf5d95c85a7e7caa47d5`  
		Last Modified: Fri, 24 Jun 2022 13:23:12 GMT  
		Size: 1.8 MB (1757341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f801ab9ea16eccd5174b433c41c9c2115d4edbc5be7dca94a73575c4e820fd9d`  
		Last Modified: Fri, 24 Jun 2022 13:23:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b75f33cc6e0d915b930696e2d8ee027ea6f65532c5e4d6cd17218d82d71b893`  
		Last Modified: Fri, 24 Jun 2022 13:23:14 GMT  
		Size: 3.4 MB (3388638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b7b0bcfe02857d9218a69ad58e74962bf0e622f18e488ad82586f11fed524005
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125264524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ebfcc33acc60d9636f256b51d5e34a7bc19f51cb10d2c8d2ab590324d34a83`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:49 GMT
ADD file:029ce6b1d94ffab93115ec72e29b81dc578e1e506b9f17808517198fa9a93144 in / 
# Thu, 23 Jun 2022 01:00:50 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 13:33:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 13:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 13:34:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 13:34:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 13:34:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 13:39:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 13:39:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 13:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 13:39:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 13:39:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 13:39:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 13:39:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 13:39:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 15:03:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 15:03:40 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 15:03:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 15:03:40 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 15:04:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 15:04:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 15:08:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 15:08:48 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 15:08:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 15:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 15:08:50 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 15:08:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 15:08:51 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 15:08:51 GMT
EXPOSE 80
# Thu, 23 Jun 2022 15:08:52 GMT
CMD ["apache2-foreground"]
# Sat, 25 Jun 2022 00:13:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Jun 2022 00:13:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 25 Jun 2022 00:41:22 GMT
ENV DRUPAL_VERSION=7.90
# Sat, 25 Jun 2022 00:41:22 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Sat, 25 Jun 2022 00:41:26 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:4a43dd1ec497b763b016923ec92796419a4f550a0b2c64b17a79c4f7f575643e`  
		Last Modified: Thu, 23 Jun 2022 01:16:47 GMT  
		Size: 22.7 MB (22748000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db582f5f0bd7b736eb381f0ee1be5bba739ff74db7bb130cf1d6b2cdca642136`  
		Last Modified: Thu, 23 Jun 2022 16:21:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ecca9394407ff4b630b7e2cedae363b82364c94764a0c7e08b819e7bfdc502`  
		Last Modified: Thu, 23 Jun 2022 16:21:45 GMT  
		Size: 59.5 MB (59539424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67065bf760ae6352f07ecd58a1802b8f25e7768aefbaa06a1c0cbec330d0f00b`  
		Last Modified: Thu, 23 Jun 2022 16:21:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d27bcf1df42da95b0d312bdd723068a750f8ffd15dfb55caab529ac457bb800`  
		Last Modified: Thu, 23 Jun 2022 16:22:17 GMT  
		Size: 17.5 MB (17479693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd0d2a7956868513d3cb462d0c1b01be75954c991e18e0740679738148415f0`  
		Last Modified: Thu, 23 Jun 2022 16:22:07 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41f15aa7b40bdd2df0554bc92b8e17d83c4470d1a197ec0b6f35fc81e05f0cb`  
		Last Modified: Thu, 23 Jun 2022 16:22:07 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2edeb01f69945118d9ff2b898d1539882155de469457051d432bb8fba404ad`  
		Last Modified: Thu, 23 Jun 2022 16:34:49 GMT  
		Size: 11.2 MB (11215036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22680c0fb0044ef84af27e97f4c0aeb21aa31217e49f64849fdac7a701ce8b5f`  
		Last Modified: Thu, 23 Jun 2022 16:34:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e6c9658b725600eacc2f45728824f65cd745e5d180d2e60d37877d06a513ff`  
		Last Modified: Thu, 23 Jun 2022 16:34:51 GMT  
		Size: 9.3 MB (9256087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd34eaab191d25f91cb60db20e91ca4300ea70ef35acaa4f46a6300714e6b3ba`  
		Last Modified: Thu, 23 Jun 2022 16:34:44 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788c2b9b589465f4d4b06aee3b3db0db502508578a5ed41e5a2de3047680c7a5`  
		Last Modified: Thu, 23 Jun 2022 16:34:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7341b11ce59b59257fe2d3ed7a00c7d58331f85aefd3da428b2e19cb58aeaf74`  
		Last Modified: Thu, 23 Jun 2022 16:34:44 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b24fd9fc228a1abbf7320ad1c167eb9d4b7eb7d5f8f068cbaf6c16ff592223`  
		Last Modified: Sat, 25 Jun 2022 01:21:56 GMT  
		Size: 1.6 MB (1631733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1620431ff2ebd0cea1db203d10c520dd2766504a9b02ff0d1cf484b8db2834`  
		Last Modified: Sat, 25 Jun 2022 01:21:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957680ce5d3610ac25b1594721ee5fc0d1586888fb6cb45925dc4e421b044b69`  
		Last Modified: Sat, 25 Jun 2022 01:41:36 GMT  
		Size: 3.4 MB (3388638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5381e7f36fc5dc6cd19d62d1d111adfddb38b861478350d95383905000af37be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140926208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3692087b566b3bec0fdec17ea3cb446209119e6dc4c3b21ba12132ed493483c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:47:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 06:47:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 06:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:47:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 06:47:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 06:52:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 06:52:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 06:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 06:52:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 06:52:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 06:52:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:52:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:52:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 07:53:23 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 07:53:24 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 07:53:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 07:53:26 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 07:53:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 07:53:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:56:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 07:56:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:56:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 07:56:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 07:56:19 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 07:56:21 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:56:21 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 07:56:22 GMT
EXPOSE 80
# Thu, 23 Jun 2022 07:56:23 GMT
CMD ["apache2-foreground"]
# Thu, 23 Jun 2022 21:51:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 21:51:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 22:04:53 GMT
ENV DRUPAL_VERSION=7.90
# Thu, 23 Jun 2022 22:04:54 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Thu, 23 Jun 2022 22:04:56 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d034d34434f4b792ee58f249f7eb03c9d05f82341f7f71967e7abde5c0af3eef`  
		Last Modified: Thu, 23 Jun 2022 08:33:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b7cfb9f69c9364d83c4565131c5cc6b0d74c1abea7e7058ad7b1d537257f7`  
		Last Modified: Thu, 23 Jun 2022 08:33:30 GMT  
		Size: 70.4 MB (70364322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4f50c99afb20799681c11e29b703209d91013affd60ce4f74a71d38bd122f5`  
		Last Modified: Thu, 23 Jun 2022 08:33:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e28f173ff95ba7e7707e0e9ca4b7b3803f2d13a6a4e85c31bc29d69d6d7f8b6`  
		Last Modified: Thu, 23 Jun 2022 08:33:54 GMT  
		Size: 18.4 MB (18366740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c57c65171ed81e89e56940dbbf006a53e1b7ae413d5bd0fe6662c162d909af9`  
		Last Modified: Thu, 23 Jun 2022 08:33:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239bdd00031a7c1ea56f72f4a9ff5c7da3b4bc9cb8c84c0abc608f9049885baa`  
		Last Modified: Thu, 23 Jun 2022 08:33:50 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0e2673060bf8b3d157b629cd94e2428aedf229e0d864d7dee063934872bb25`  
		Last Modified: Thu, 23 Jun 2022 08:41:56 GMT  
		Size: 11.0 MB (11003503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71425c52c903ed25c8a74376a7423cc779d77544e1f63126d8503286d22499a6`  
		Last Modified: Thu, 23 Jun 2022 08:41:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8107b08d5aa14548f6e7630247f26bf7f0b0bd76af225f352ddcf22395db116`  
		Last Modified: Thu, 23 Jun 2022 08:41:55 GMT  
		Size: 10.2 MB (10197860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aeae27769f64358c8bcb116bc40683a33c57e86610f88fd5683cdd08fdabf`  
		Last Modified: Thu, 23 Jun 2022 08:41:53 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a5d16c633ed3b510701b876ded184a9892ebd8d4c30560bc7fff45719ff1d`  
		Last Modified: Thu, 23 Jun 2022 08:41:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3919a89990bfdfa3b09ef33322bafab428412b1731ce100b20c8414bc8717b`  
		Last Modified: Thu, 23 Jun 2022 08:41:53 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b997480e6b33c0d8ade80baa56deb048443aacf2d63845725ad96cf550307c01`  
		Last Modified: Thu, 23 Jun 2022 22:25:10 GMT  
		Size: 1.7 MB (1685696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3ede81cefb35118adaa0a607e3bfcfd235b93b8fd20e045b2d93f655572802`  
		Last Modified: Thu, 23 Jun 2022 22:25:10 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc2891d559847f726a8a99e1aeea09dbc8bae6709f88ec2d2b46f76d824b7ce`  
		Last Modified: Thu, 23 Jun 2022 22:35:50 GMT  
		Size: 3.4 MB (3388282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:b2b9b6973af8db3c7bb86960a19f6c6eced02f7b1a5b2473a8a27ba2193c33ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155358780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e90c0050100373b6b129b93d958f691e5a432847ae86f977f73e3856ad9a75`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:59 GMT
ADD file:d4d6ebbe6e038ac58e266fb07bee755ccccf597fb15b3e8264165279e8fbed3b in / 
# Thu, 23 Jun 2022 00:40:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 11:54:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 11:54:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 11:55:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 11:55:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 11:55:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 11:58:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 11:58:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 11:58:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 11:58:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 11:58:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 11:58:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 11:58:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 11:58:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 12:49:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 12:50:00 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 12:50:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 12:50:02 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 12:50:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 12:50:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 12:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 12:52:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 12:52:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 12:52:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 12:52:52 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 12:52:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 12:52:54 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 12:52:55 GMT
EXPOSE 80
# Thu, 23 Jun 2022 12:52:56 GMT
CMD ["apache2-foreground"]
# Thu, 23 Jun 2022 16:39:33 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 16:39:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 16:51:05 GMT
ENV DRUPAL_VERSION=7.90
# Thu, 23 Jun 2022 16:51:05 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Thu, 23 Jun 2022 16:51:07 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:e8877ae0470a67233ffd6b1ee842fc356ff46b5b3c594a02395801f85ccec7b4`  
		Last Modified: Thu, 23 Jun 2022 00:47:36 GMT  
		Size: 27.8 MB (27799542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5c149d286aea4ad057b015b69d3281c0af0efce4aa4e8285433721af2b9eb7`  
		Last Modified: Thu, 23 Jun 2022 13:28:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82160afe245a35bfb9dce3c758338e3f6667bcef318602ee2d815e07bf8051a`  
		Last Modified: Thu, 23 Jun 2022 13:29:09 GMT  
		Size: 81.2 MB (81228465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc126f6acc245f7df92152a426f111932f4cf4a526b092893121f08d3b9e7acd`  
		Last Modified: Thu, 23 Jun 2022 13:28:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fccc0c8bfd9326b665f8523e5d63e1d2c4e6a7cc0a68687ff95078efa08fec`  
		Last Modified: Thu, 23 Jun 2022 13:29:34 GMT  
		Size: 18.9 MB (18900254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20932e82001cab6dd906a468440f620b7edb8353c5c2ea1eccd2788ffedc2e`  
		Last Modified: Thu, 23 Jun 2022 13:29:30 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a698cedd07bea176f834a5f21b62e352bed5be2618b6d57c30076eb6b6b3d3fc`  
		Last Modified: Thu, 23 Jun 2022 13:29:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc3eb3fe798e887df0e6531e7506537699d74d0de087b3b161f2e6200b96c22`  
		Last Modified: Thu, 23 Jun 2022 13:38:16 GMT  
		Size: 11.0 MB (11003986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ff1e79031be3783d3d4fe8f98071d1b2a4f376af6f9f8e8ec9ae1b69b7d4a`  
		Last Modified: Thu, 23 Jun 2022 13:38:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4299f41a05600627926c2ca7da19b386280cd393e8a4746859281390b70a42ba`  
		Last Modified: Thu, 23 Jun 2022 13:38:13 GMT  
		Size: 10.9 MB (10931821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3730b6b01bb354c0be032497aaf7bcadd9ba49b8289fa85d7b088ab12e3444`  
		Last Modified: Thu, 23 Jun 2022 13:38:11 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466900b2a87eb46141a712c473228b79222e3449855d15ff2690f9433f1c35a1`  
		Last Modified: Thu, 23 Jun 2022 13:38:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48df5362a11710de22171a37740cdadf5969ce2ead0b0216c7a0d48f87f02b88`  
		Last Modified: Thu, 23 Jun 2022 13:38:11 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846687e41c6e381af66370eb8ea63a27ba7c0cb78dfd48b935037f6772033e06`  
		Last Modified: Thu, 23 Jun 2022 17:12:47 GMT  
		Size: 2.1 MB (2100652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09164ec6fc2ada5bceea476cf3157675f5012441be3bd7f5b64b942f959304`  
		Last Modified: Thu, 23 Jun 2022 17:12:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1430ded0e9a8988d110ae477ade60bf17e7449c89b00aee0817d11d1f70ca7f6`  
		Last Modified: Thu, 23 Jun 2022 17:24:02 GMT  
		Size: 3.4 MB (3388278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; mips64le

```console
$ docker pull drupal@sha256:76e44e10193d1bb0621ffcdd0cf15840aa866d8fd4e7fff4d761db556a5e67dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131566797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7f8022d8b24f73c965925341c678bd2308760fc9b8c5ce33d1436de8f3c664`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 May 2022 01:12:21 GMT
ADD file:12eb3f58e1c47ef1af98f481c1f5f33832f45144bf66f3a01065f8c939f1eaa9 in / 
# Sat, 28 May 2022 01:12:25 GMT
CMD ["bash"]
# Sat, 28 May 2022 04:30:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 May 2022 04:30:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 May 2022 04:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 04:32:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 May 2022 04:32:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 May 2022 04:47:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 May 2022 04:47:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 May 2022 04:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 May 2022 04:48:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 May 2022 04:48:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 May 2022 04:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 04:48:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 04:48:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 May 2022 06:40:55 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 10 Jun 2022 03:51:59 GMT
ENV PHP_VERSION=8.0.20
# Fri, 10 Jun 2022 03:52:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Fri, 10 Jun 2022 03:52:06 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Fri, 10 Jun 2022 03:52:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jun 2022 03:52:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jun 2022 04:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 Jun 2022 04:06:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 Jun 2022 04:06:14 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jun 2022 04:06:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jun 2022 04:06:21 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Jun 2022 04:06:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 Jun 2022 04:06:27 GMT
WORKDIR /var/www/html
# Fri, 10 Jun 2022 04:06:31 GMT
EXPOSE 80
# Fri, 10 Jun 2022 04:06:34 GMT
CMD ["apache2-foreground"]
# Mon, 13 Jun 2022 23:16:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 23:16:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 13 Jun 2022 23:16:45 GMT
ENV DRUPAL_VERSION=7.90
# Mon, 13 Jun 2022 23:16:48 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Mon, 13 Jun 2022 23:16:58 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:79a954ba282b6c17b5d2fdc4563e0fbc4bf4e3c673bada0b2f656937656557eb`  
		Last Modified: Sat, 28 May 2022 01:22:56 GMT  
		Size: 25.8 MB (25814580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6936d9097093c4664cd64eba7be21857248e25815188f5cd5cf9fbcb8e4d78e`  
		Last Modified: Sat, 28 May 2022 10:46:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcae9ccf6d5b052c23cebff05a2012ffdbca17b5f4a3cfd4e15967511468db7`  
		Last Modified: Sat, 28 May 2022 10:47:00 GMT  
		Size: 61.4 MB (61409252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c4f1e6032f61dcf0afbf3f69326d6b5c7083ea1aa05e647dca92554e81feb`  
		Last Modified: Sat, 28 May 2022 10:46:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320c4a59ecb53e017b592415294e59d3208e6dfd3cfd218b17253881d2d65a88`  
		Last Modified: Sat, 28 May 2022 10:47:41 GMT  
		Size: 18.4 MB (18402037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33cc5eaba3216d579993416e1889bafa22eeda65ac6afa241d11c73ed80db36`  
		Last Modified: Sat, 28 May 2022 10:47:29 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a55d5695485937d3da6b1f0e50bba4e8693396ce65b3270441f8fb99c43c05`  
		Last Modified: Sat, 28 May 2022 10:47:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8964f5ca8afe4d49a69095b3c11c17b3ae5b54390ef5fc94c185955b082fc46b`  
		Last Modified: Fri, 10 Jun 2022 06:13:16 GMT  
		Size: 11.0 MB (11002421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b33950860b90390c3a8347aae18a770a11f833a68540855bd839f153107b96`  
		Last Modified: Fri, 10 Jun 2022 06:13:11 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0acd50068549a36932ff5c4aa6824b9ecdc1090f5360648a10c25826a64850`  
		Last Modified: Fri, 10 Jun 2022 06:13:19 GMT  
		Size: 9.9 MB (9876811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4097209346df97a18e1c0004d857baec6bbb4b2d7e4added0a1860dbce409bc3`  
		Last Modified: Fri, 10 Jun 2022 06:13:11 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ab4159d1cbbf1581495258987fa44bc05145a120bf272d40836db787f9dd0`  
		Last Modified: Fri, 10 Jun 2022 06:13:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59093e5b3133fed603b3ca3d7edf624215f3f080b7a4f48b6acd8b2828e0e67b`  
		Last Modified: Fri, 10 Jun 2022 06:13:11 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b73fef68e19a2b2aceb53cc82065e2363381083ec190a8a5ccff0ac4f1deb8`  
		Last Modified: Mon, 13 Jun 2022 23:21:52 GMT  
		Size: 1.7 MB (1667611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cad2d711819b9f01f71c492132fddf018f6a2fbae8c0ba24ee2b02cd3c47ecb`  
		Last Modified: Mon, 13 Jun 2022 23:21:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d2694d4fa57434882521d4604f40a2c6cc1d987515c0f906fb5d6959206eeb`  
		Last Modified: Mon, 13 Jun 2022 23:21:54 GMT  
		Size: 3.4 MB (3388279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; ppc64le

```console
$ docker pull drupal@sha256:392779464170aa187e39bf2d33493983a100e43db8ef98e7c998b603f033278e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160525520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e788ba5d2e387eb561670802ad2a34fdbc78b1d41dfd22698c1d1df815f66fe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 02:03:29 GMT
ADD file:72c3739ee19c484811115caacd1b2bf903a764246b77af65c098817e5a13f8ca in / 
# Thu, 23 Jun 2022 02:03:32 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 13:57:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 13:58:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 14:02:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 14:02:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 14:02:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 14:09:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 14:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 14:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 14:11:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 14:11:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 14:11:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 14:11:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 14:11:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 16:25:03 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 16:25:05 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 16:25:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 16:25:12 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 16:26:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 16:26:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 16:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 16:34:06 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 16:34:11 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 16:34:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 16:34:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 16:34:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 16:34:19 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 16:34:21 GMT
EXPOSE 80
# Thu, 23 Jun 2022 16:34:23 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jun 2022 11:56:06 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 11:56:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jun 2022 12:34:09 GMT
ENV DRUPAL_VERSION=7.90
# Fri, 24 Jun 2022 12:34:12 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Fri, 24 Jun 2022 12:34:30 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:18188ef7804b6b81fced393814287e8c6e18656751108acdbbd364d57775a243`  
		Last Modified: Thu, 23 Jun 2022 02:17:52 GMT  
		Size: 30.6 MB (30560321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2877e8479db46f29bb54ac758acfe651da84aefe1b9543a13838915d6800465`  
		Last Modified: Thu, 23 Jun 2022 17:37:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30446a3cc0e690c09fe51389b94fa6f6ffbf5e2f269541d2b70de4db3a1019a3`  
		Last Modified: Thu, 23 Jun 2022 17:37:58 GMT  
		Size: 82.3 MB (82294473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9b735ef7ac827069c9f2f3ccc59e8da89b92f9a15d2f5c2f6c2cde756c73b1`  
		Last Modified: Thu, 23 Jun 2022 17:37:37 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cc92a1332be984b5149e1291aa31938522205f57d5f02da8ec0b459f128c3c`  
		Last Modified: Thu, 23 Jun 2022 17:38:25 GMT  
		Size: 19.8 MB (19822318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6347b18d5bfa79e1c438e531822575b167cb1a2437d69b8da87428ee9bb89fe7`  
		Last Modified: Thu, 23 Jun 2022 17:38:21 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efe91d214690f87077b8993e71b640b8d409c8ed303d70e30c139336fe515d2`  
		Last Modified: Thu, 23 Jun 2022 17:38:21 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08b14355bd45ace6d24d30c1b74f21fd2e6d9940ab0ff01dc9b40512fd6c60`  
		Last Modified: Thu, 23 Jun 2022 17:47:45 GMT  
		Size: 11.2 MB (11216705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed31504b58c88ccf926ed5f0ba8ce53e2f2b82b1a5dc47aab5587822701fb06c`  
		Last Modified: Thu, 23 Jun 2022 17:47:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b6bcba72192e9103eb84b73a5ab4b04db16a771b3b7333e3b006d8adfd9433`  
		Last Modified: Thu, 23 Jun 2022 17:47:43 GMT  
		Size: 11.1 MB (11087855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a937e983d6d4aea7899aed003d7c561ccbba09f07a53df09fc330ede92b3053e`  
		Last Modified: Thu, 23 Jun 2022 17:47:41 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421a1ff43149465d04f9aa1755ff67e72d0528024420428d968accf6ce774e7c`  
		Last Modified: Thu, 23 Jun 2022 17:47:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbacd1e3f728fdd405aafd29aa8bc1010acd926e09e16b9347066954180f0d89`  
		Last Modified: Thu, 23 Jun 2022 17:47:40 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b71948f35f20216a9ac5496c9ff44de0bc962d5cfedf7ee9aae2a306a6f0dfb`  
		Last Modified: Fri, 24 Jun 2022 13:18:15 GMT  
		Size: 2.1 MB (2149287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfa53a77105897a991d2304589a945a3b8a79e11579099bbdc96bf02e3889a3`  
		Last Modified: Fri, 24 Jun 2022 13:18:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b3ba11abd6c3dfe67c40e75e772e9812ce0da1df53837c0e2a0c17f805a962`  
		Last Modified: Fri, 24 Jun 2022 13:56:02 GMT  
		Size: 3.4 MB (3388638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; s390x

```console
$ docker pull drupal@sha256:c3ae2de76ac70a80b253c56cf6c224f00ca7221037bdbe4f90b046b7fcd2fc7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135332721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0673f2143075c219f815ef3b3325f5e00a1c5ca04cca80e4b3a2d886ff22c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Jun 2022 00:44:04 GMT
ADD file:b5735387132c5d35278da27339d76ef4a166c7ea012cfe13bd542fd5f0055fb4 in / 
# Thu, 23 Jun 2022 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:34:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 06:34:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 06:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:35:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 06:35:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 06:37:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Jun 2022 06:37:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Jun 2022 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Jun 2022 06:37:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Jun 2022 06:37:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Jun 2022 06:37:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:37:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:37:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 07:21:51 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 23 Jun 2022 07:21:51 GMT
ENV PHP_VERSION=8.0.20
# Thu, 23 Jun 2022 07:21:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Thu, 23 Jun 2022 07:21:52 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Thu, 23 Jun 2022 07:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 07:22:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:24:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 07:24:16 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:24:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 07:24:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 07:24:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Jun 2022 07:24:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:24:17 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 07:24:17 GMT
EXPOSE 80
# Thu, 23 Jun 2022 07:24:18 GMT
CMD ["apache2-foreground"]
# Thu, 23 Jun 2022 19:34:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 19:34:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 19:48:46 GMT
ENV DRUPAL_VERSION=7.90
# Thu, 23 Jun 2022 19:48:46 GMT
ENV DRUPAL_MD5=4cb30e74d1b57ef32d8efcd664e32f54
# Thu, 23 Jun 2022 19:48:47 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:34b063f6640cedaaed5292721bedcce5039c2e2c11d3168badb2d90259505d49`  
		Last Modified: Thu, 23 Jun 2022 00:52:35 GMT  
		Size: 25.8 MB (25758710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8357c4b02deef8ecce801495e93f5c4242cf7900e112d6776b08a230c274552`  
		Last Modified: Thu, 23 Jun 2022 07:58:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3169fc154c33291175b971afc7c65958bb32d8b8f165c05bee593b6c64258b`  
		Last Modified: Thu, 23 Jun 2022 07:58:24 GMT  
		Size: 64.7 MB (64727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685acc3dbe56641d8296e5a22dc5a29b1e35bfe270094fec5f843ecfe07ee64a`  
		Last Modified: Thu, 23 Jun 2022 07:58:14 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77229c38c9f4d94a006ed8fbd4724bc9edd04bab85f8cddf0fc742794c4cde99`  
		Last Modified: Thu, 23 Jun 2022 07:58:39 GMT  
		Size: 18.5 MB (18524899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073f20375e0255cef87de9f7fb94ba8bc314de9c66d74e897d5c07ae0d05a985`  
		Last Modified: Thu, 23 Jun 2022 07:58:36 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87369ad9dc1c31dc03ab254a4b3a98b981dbcd016105a134c4321d5e995dbe7`  
		Last Modified: Thu, 23 Jun 2022 07:58:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcbdc05d83163b13752aaa50bf1ef51fe7903281e4813245aed06041bd7a809`  
		Last Modified: Thu, 23 Jun 2022 08:04:29 GMT  
		Size: 11.2 MB (11215206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe0fa9a9e33b7bca36c56b0dc082619b3869316b4bd5f76ada8072a449af0f5`  
		Last Modified: Thu, 23 Jun 2022 08:04:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921d8f637c10c644d80175e747b25604f5d69b3bd80a0241bf92684aba2fc8f`  
		Last Modified: Thu, 23 Jun 2022 08:04:29 GMT  
		Size: 9.9 MB (9854778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d025fd918ffc85b6e7f1754b1c70bb100d83f744d2b41ac60267427e44ef046f`  
		Last Modified: Thu, 23 Jun 2022 08:04:28 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa935d354d69d68f7ed2dba080ecfdd19ab9b75b051f511d1b8495b0a662e4`  
		Last Modified: Thu, 23 Jun 2022 08:04:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854699bf98e4c2f5cf3676202d74403d1caa02b7fbe4a68adaa95bdf46eccca9`  
		Last Modified: Thu, 23 Jun 2022 08:04:28 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c402a153d86287fd55719350fe7fed060af2d997589a8c6b73f6ecc5a8f975f6`  
		Last Modified: Thu, 23 Jun 2022 20:12:21 GMT  
		Size: 1.9 MB (1857584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e30eda5e19e509b619e292197c3b4ffb54a5c6bbb09efad6df5d9e3bcf6b7f4`  
		Last Modified: Thu, 23 Jun 2022 20:12:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a871e5d487a725f7941cc7df20986058b806a925e3e4b65d81cb5ab8a8e7b97e`  
		Last Modified: Thu, 23 Jun 2022 20:25:06 GMT  
		Size: 3.4 MB (3388626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
