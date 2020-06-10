<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1.13`](#backdrop113)
-	[`backdrop:1.13.2`](#backdrop1132)
-	[`backdrop:1.13.2-apache`](#backdrop1132-apache)
-	[`backdrop:1.13.2-fpm`](#backdrop1132-fpm)
-	[`backdrop:1.13-apache`](#backdrop113-apache)
-	[`backdrop:1.13-fpm`](#backdrop113-fpm)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13.2`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13.2` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13.2` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13.2-apache`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13.2-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13.2-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13.2-fpm`

```console
$ docker pull backdrop@sha256:280e8138a2042dda4ee24d52f2e9c2c22769ec59baabdc57090651be392ee020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13.2-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:80fe4ac5cfb4a961007f8458586aee36db7ce4b3f96a6b786c56537f3b6a2426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155970302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5425f1214932c6b99bc4db3548202b15cd2853822a52709c074897d30bd6737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:28:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:28:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:28:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:28 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:29 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:30 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:27:31 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:27:31 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 21:59:21 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:59:21 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:59:25 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:59:25 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:59:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae949b426cac5a3463facc13c668f88522032082a1d83f5de97accfa82cb5d5d`  
		Last Modified: Fri, 15 May 2020 15:11:25 GMT  
		Size: 12.6 MB (12632189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6d1b6b568503a3b6a05b6ba0ccde1b647aa68cd67c4f0534ae9535b8670565`  
		Last Modified: Fri, 15 May 2020 15:11:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e951ec576f29ec876d54181bce00fe24e4dad23eba9ff710e5d92aa9ac91e87d`  
		Last Modified: Fri, 15 May 2020 15:11:29 GMT  
		Size: 28.5 MB (28529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e29517811babd161b6d45af1b8d634d1b15de13df9af1a15195677fc6b35de`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e33c96f760ecf1a2f7163e84989556d7b3e7be84db5f2e7ab63698f96ffb03`  
		Last Modified: Tue, 02 Jun 2020 21:32:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7fe3ca444b58234820fc66c4d1d1b15727ff1a42939c93f5657a63be121b`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7992c584898ed4deef96b00167517b9f6aad1aea6c88f63f50b5c67dee7c3`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 7.8 KB (7794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba57594ccca56daf97f1efde5a27ed84ad8db52f2b715d06367cff8ec76c78`  
		Last Modified: Tue, 02 Jun 2020 21:59:50 GMT  
		Size: 2.6 MB (2576724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f7df9bc5b2870858579f1dbf81f046cde186784e6331ef80e2605b91dd313`  
		Last Modified: Tue, 02 Jun 2020 21:59:51 GMT  
		Size: 8.5 MB (8468670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140f5221daf2f74514284852c9ae84de834d23af24223b681bffd230ff2cc53`  
		Last Modified: Tue, 02 Jun 2020 21:59:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13.2-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3f90e5b33341a7a655fc2dedd4b74a42e0718fc29d07cadfffbef66d50395dcb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148055280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b98c5a85a41ff91179db7a7b43eab764693b7a6e89da5be10a4091066f58fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:29:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:29:44 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:30:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:33:49 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:33:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:33:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:33:55 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:33:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 09 Jun 2020 11:33:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Jun 2020 11:33:58 GMT
EXPOSE 9000
# Tue, 09 Jun 2020 11:33:59 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2020 01:30:42 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:30:44 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:30:46 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:30:48 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:30:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:30:56 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:30:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af7dea9c098c2e28e5fb4924011e11e5c7ee1044ceea90d32824c7e063bea9`  
		Last Modified: Tue, 09 Jun 2020 12:02:06 GMT  
		Size: 12.6 MB (12631068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4467340b1a31af0dda4ff32aedb946b3f1acc745e4cb6f9d8ef2bbf3fa47f4`  
		Last Modified: Tue, 09 Jun 2020 12:02:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707cc9f21c1226118afe85750aef1153024067ac302cdd449275073c31399688`  
		Last Modified: Tue, 09 Jun 2020 12:02:11 GMT  
		Size: 28.2 MB (28205762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a991081cc60ffd96f5d934f79cedc2835e6055a5cab038fbd396adafa844e609`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8f300c1d563640b9fe51bbb7517b91172b622fc902a553a139f773dbf43359`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f8967541a857e8ee20073c42191081a4e9b37ccd2212feca3a6804e31ed66`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4861f1f4ea5c5f059169cb1a9d6851c183ab686a6c9d47ff2a9a049b3899a4d`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 7.8 KB (7781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1115b020a1d6b25b98b45d52d94e5be95e50b125eb162151d3ced05dafafa9c6`  
		Last Modified: Wed, 10 Jun 2020 01:31:43 GMT  
		Size: 2.5 MB (2542096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2d338f21fb73d0a5f9773fa21f03abd65d34c309bd28fd53d139552a6e9ae`  
		Last Modified: Wed, 10 Jun 2020 01:31:46 GMT  
		Size: 8.5 MB (8468809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb362d10fa8f7e466d425ff0120be38ef9c41a427d9ec18fdcbe72bf9704af30`  
		Last Modified: Wed, 10 Jun 2020 01:31:42 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13-apache`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.13-fpm`

```console
$ docker pull backdrop@sha256:280e8138a2042dda4ee24d52f2e9c2c22769ec59baabdc57090651be392ee020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.13-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:80fe4ac5cfb4a961007f8458586aee36db7ce4b3f96a6b786c56537f3b6a2426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155970302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5425f1214932c6b99bc4db3548202b15cd2853822a52709c074897d30bd6737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:28:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:28:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:28:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:28 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:29 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:30 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:27:31 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:27:31 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 21:59:21 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:59:21 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:59:25 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:59:25 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:59:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae949b426cac5a3463facc13c668f88522032082a1d83f5de97accfa82cb5d5d`  
		Last Modified: Fri, 15 May 2020 15:11:25 GMT  
		Size: 12.6 MB (12632189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6d1b6b568503a3b6a05b6ba0ccde1b647aa68cd67c4f0534ae9535b8670565`  
		Last Modified: Fri, 15 May 2020 15:11:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e951ec576f29ec876d54181bce00fe24e4dad23eba9ff710e5d92aa9ac91e87d`  
		Last Modified: Fri, 15 May 2020 15:11:29 GMT  
		Size: 28.5 MB (28529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e29517811babd161b6d45af1b8d634d1b15de13df9af1a15195677fc6b35de`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e33c96f760ecf1a2f7163e84989556d7b3e7be84db5f2e7ab63698f96ffb03`  
		Last Modified: Tue, 02 Jun 2020 21:32:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7fe3ca444b58234820fc66c4d1d1b15727ff1a42939c93f5657a63be121b`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7992c584898ed4deef96b00167517b9f6aad1aea6c88f63f50b5c67dee7c3`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 7.8 KB (7794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba57594ccca56daf97f1efde5a27ed84ad8db52f2b715d06367cff8ec76c78`  
		Last Modified: Tue, 02 Jun 2020 21:59:50 GMT  
		Size: 2.6 MB (2576724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f7df9bc5b2870858579f1dbf81f046cde186784e6331ef80e2605b91dd313`  
		Last Modified: Tue, 02 Jun 2020 21:59:51 GMT  
		Size: 8.5 MB (8468670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140f5221daf2f74514284852c9ae84de834d23af24223b681bffd230ff2cc53`  
		Last Modified: Tue, 02 Jun 2020 21:59:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.13-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3f90e5b33341a7a655fc2dedd4b74a42e0718fc29d07cadfffbef66d50395dcb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148055280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b98c5a85a41ff91179db7a7b43eab764693b7a6e89da5be10a4091066f58fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:29:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:29:44 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:30:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:33:49 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:33:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:33:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:33:55 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:33:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 09 Jun 2020 11:33:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Jun 2020 11:33:58 GMT
EXPOSE 9000
# Tue, 09 Jun 2020 11:33:59 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2020 01:30:42 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:30:44 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:30:46 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:30:48 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:30:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:30:56 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:30:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af7dea9c098c2e28e5fb4924011e11e5c7ee1044ceea90d32824c7e063bea9`  
		Last Modified: Tue, 09 Jun 2020 12:02:06 GMT  
		Size: 12.6 MB (12631068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4467340b1a31af0dda4ff32aedb946b3f1acc745e4cb6f9d8ef2bbf3fa47f4`  
		Last Modified: Tue, 09 Jun 2020 12:02:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707cc9f21c1226118afe85750aef1153024067ac302cdd449275073c31399688`  
		Last Modified: Tue, 09 Jun 2020 12:02:11 GMT  
		Size: 28.2 MB (28205762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a991081cc60ffd96f5d934f79cedc2835e6055a5cab038fbd396adafa844e609`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8f300c1d563640b9fe51bbb7517b91172b622fc902a553a139f773dbf43359`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f8967541a857e8ee20073c42191081a4e9b37ccd2212feca3a6804e31ed66`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4861f1f4ea5c5f059169cb1a9d6851c183ab686a6c9d47ff2a9a049b3899a4d`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 7.8 KB (7781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1115b020a1d6b25b98b45d52d94e5be95e50b125eb162151d3ced05dafafa9c6`  
		Last Modified: Wed, 10 Jun 2020 01:31:43 GMT  
		Size: 2.5 MB (2542096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2d338f21fb73d0a5f9773fa21f03abd65d34c309bd28fd53d139552a6e9ae`  
		Last Modified: Wed, 10 Jun 2020 01:31:46 GMT  
		Size: 8.5 MB (8468809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb362d10fa8f7e466d425ff0120be38ef9c41a427d9ec18fdcbe72bf9704af30`  
		Last Modified: Wed, 10 Jun 2020 01:31:42 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:280e8138a2042dda4ee24d52f2e9c2c22769ec59baabdc57090651be392ee020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:80fe4ac5cfb4a961007f8458586aee36db7ce4b3f96a6b786c56537f3b6a2426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155970302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5425f1214932c6b99bc4db3548202b15cd2853822a52709c074897d30bd6737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:28:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:28:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:28:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:28 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:29 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:30 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:27:31 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:27:31 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 21:59:21 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:59:21 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:59:25 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:59:25 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:59:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae949b426cac5a3463facc13c668f88522032082a1d83f5de97accfa82cb5d5d`  
		Last Modified: Fri, 15 May 2020 15:11:25 GMT  
		Size: 12.6 MB (12632189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6d1b6b568503a3b6a05b6ba0ccde1b647aa68cd67c4f0534ae9535b8670565`  
		Last Modified: Fri, 15 May 2020 15:11:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e951ec576f29ec876d54181bce00fe24e4dad23eba9ff710e5d92aa9ac91e87d`  
		Last Modified: Fri, 15 May 2020 15:11:29 GMT  
		Size: 28.5 MB (28529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e29517811babd161b6d45af1b8d634d1b15de13df9af1a15195677fc6b35de`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e33c96f760ecf1a2f7163e84989556d7b3e7be84db5f2e7ab63698f96ffb03`  
		Last Modified: Tue, 02 Jun 2020 21:32:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7fe3ca444b58234820fc66c4d1d1b15727ff1a42939c93f5657a63be121b`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7992c584898ed4deef96b00167517b9f6aad1aea6c88f63f50b5c67dee7c3`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 7.8 KB (7794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba57594ccca56daf97f1efde5a27ed84ad8db52f2b715d06367cff8ec76c78`  
		Last Modified: Tue, 02 Jun 2020 21:59:50 GMT  
		Size: 2.6 MB (2576724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f7df9bc5b2870858579f1dbf81f046cde186784e6331ef80e2605b91dd313`  
		Last Modified: Tue, 02 Jun 2020 21:59:51 GMT  
		Size: 8.5 MB (8468670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140f5221daf2f74514284852c9ae84de834d23af24223b681bffd230ff2cc53`  
		Last Modified: Tue, 02 Jun 2020 21:59:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3f90e5b33341a7a655fc2dedd4b74a42e0718fc29d07cadfffbef66d50395dcb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148055280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b98c5a85a41ff91179db7a7b43eab764693b7a6e89da5be10a4091066f58fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:29:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:29:44 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:30:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:33:49 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:33:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:33:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:33:55 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:33:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 09 Jun 2020 11:33:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Jun 2020 11:33:58 GMT
EXPOSE 9000
# Tue, 09 Jun 2020 11:33:59 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2020 01:30:42 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:30:44 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:30:46 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:30:48 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:30:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:30:56 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:30:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af7dea9c098c2e28e5fb4924011e11e5c7ee1044ceea90d32824c7e063bea9`  
		Last Modified: Tue, 09 Jun 2020 12:02:06 GMT  
		Size: 12.6 MB (12631068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4467340b1a31af0dda4ff32aedb946b3f1acc745e4cb6f9d8ef2bbf3fa47f4`  
		Last Modified: Tue, 09 Jun 2020 12:02:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707cc9f21c1226118afe85750aef1153024067ac302cdd449275073c31399688`  
		Last Modified: Tue, 09 Jun 2020 12:02:11 GMT  
		Size: 28.2 MB (28205762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a991081cc60ffd96f5d934f79cedc2835e6055a5cab038fbd396adafa844e609`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8f300c1d563640b9fe51bbb7517b91172b622fc902a553a139f773dbf43359`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f8967541a857e8ee20073c42191081a4e9b37ccd2212feca3a6804e31ed66`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4861f1f4ea5c5f059169cb1a9d6851c183ab686a6c9d47ff2a9a049b3899a4d`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 7.8 KB (7781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1115b020a1d6b25b98b45d52d94e5be95e50b125eb162151d3ced05dafafa9c6`  
		Last Modified: Wed, 10 Jun 2020 01:31:43 GMT  
		Size: 2.5 MB (2542096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2d338f21fb73d0a5f9773fa21f03abd65d34c309bd28fd53d139552a6e9ae`  
		Last Modified: Wed, 10 Jun 2020 01:31:46 GMT  
		Size: 8.5 MB (8468809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb362d10fa8f7e466d425ff0120be38ef9c41a427d9ec18fdcbe72bf9704af30`  
		Last Modified: Wed, 10 Jun 2020 01:31:42 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:280e8138a2042dda4ee24d52f2e9c2c22769ec59baabdc57090651be392ee020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:80fe4ac5cfb4a961007f8458586aee36db7ce4b3f96a6b786c56537f3b6a2426
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155970302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5425f1214932c6b99bc4db3548202b15cd2853822a52709c074897d30bd6737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:54:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:28:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:28:11 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:28:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:28:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:28 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:29 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:30 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 02 Jun 2020 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2020 21:27:31 GMT
EXPOSE 9000
# Tue, 02 Jun 2020 21:27:31 GMT
CMD ["php-fpm"]
# Tue, 02 Jun 2020 21:59:21 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:59:21 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:59:21 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:59:25 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:59:25 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:59:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:59:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae949b426cac5a3463facc13c668f88522032082a1d83f5de97accfa82cb5d5d`  
		Last Modified: Fri, 15 May 2020 15:11:25 GMT  
		Size: 12.6 MB (12632189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6d1b6b568503a3b6a05b6ba0ccde1b647aa68cd67c4f0534ae9535b8670565`  
		Last Modified: Fri, 15 May 2020 15:11:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e951ec576f29ec876d54181bce00fe24e4dad23eba9ff710e5d92aa9ac91e87d`  
		Last Modified: Fri, 15 May 2020 15:11:29 GMT  
		Size: 28.5 MB (28529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e29517811babd161b6d45af1b8d634d1b15de13df9af1a15195677fc6b35de`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e33c96f760ecf1a2f7163e84989556d7b3e7be84db5f2e7ab63698f96ffb03`  
		Last Modified: Tue, 02 Jun 2020 21:32:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7fe3ca444b58234820fc66c4d1d1b15727ff1a42939c93f5657a63be121b`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e7992c584898ed4deef96b00167517b9f6aad1aea6c88f63f50b5c67dee7c3`  
		Last Modified: Tue, 02 Jun 2020 21:32:32 GMT  
		Size: 7.8 KB (7794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba57594ccca56daf97f1efde5a27ed84ad8db52f2b715d06367cff8ec76c78`  
		Last Modified: Tue, 02 Jun 2020 21:59:50 GMT  
		Size: 2.6 MB (2576724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f7df9bc5b2870858579f1dbf81f046cde186784e6331ef80e2605b91dd313`  
		Last Modified: Tue, 02 Jun 2020 21:59:51 GMT  
		Size: 8.5 MB (8468670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140f5221daf2f74514284852c9ae84de834d23af24223b681bffd230ff2cc53`  
		Last Modified: Tue, 02 Jun 2020 21:59:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3f90e5b33341a7a655fc2dedd4b74a42e0718fc29d07cadfffbef66d50395dcb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148055280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b98c5a85a41ff91179db7a7b43eab764693b7a6e89da5be10a4091066f58fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 09 Jun 2020 10:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:33:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:29:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:29:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:29:44 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:30:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:33:49 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:33:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:33:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:33:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:33:55 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:33:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 09 Jun 2020 11:33:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Jun 2020 11:33:58 GMT
EXPOSE 9000
# Tue, 09 Jun 2020 11:33:59 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2020 01:30:42 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:30:44 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:30:46 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:30:48 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:30:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:30:56 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:30:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:30:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85af7dea9c098c2e28e5fb4924011e11e5c7ee1044ceea90d32824c7e063bea9`  
		Last Modified: Tue, 09 Jun 2020 12:02:06 GMT  
		Size: 12.6 MB (12631068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4467340b1a31af0dda4ff32aedb946b3f1acc745e4cb6f9d8ef2bbf3fa47f4`  
		Last Modified: Tue, 09 Jun 2020 12:02:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707cc9f21c1226118afe85750aef1153024067ac302cdd449275073c31399688`  
		Last Modified: Tue, 09 Jun 2020 12:02:11 GMT  
		Size: 28.2 MB (28205762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a991081cc60ffd96f5d934f79cedc2835e6055a5cab038fbd396adafa844e609`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8f300c1d563640b9fe51bbb7517b91172b622fc902a553a139f773dbf43359`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f8967541a857e8ee20073c42191081a4e9b37ccd2212feca3a6804e31ed66`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4861f1f4ea5c5f059169cb1a9d6851c183ab686a6c9d47ff2a9a049b3899a4d`  
		Last Modified: Tue, 09 Jun 2020 12:02:03 GMT  
		Size: 7.8 KB (7781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1115b020a1d6b25b98b45d52d94e5be95e50b125eb162151d3ced05dafafa9c6`  
		Last Modified: Wed, 10 Jun 2020 01:31:43 GMT  
		Size: 2.5 MB (2542096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2d338f21fb73d0a5f9773fa21f03abd65d34c309bd28fd53d139552a6e9ae`  
		Last Modified: Wed, 10 Jun 2020 01:31:46 GMT  
		Size: 8.5 MB (8468809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb362d10fa8f7e466d425ff0120be38ef9c41a427d9ec18fdcbe72bf9704af30`  
		Last Modified: Wed, 10 Jun 2020 01:31:42 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:6ecbfae500ec9fc6895427083f26242f6a5e317e7827d564cfc813d9d8258882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:311eb5f76bcbee1ec07d07576b28eaa0f64c70804b377df7263ab66d841e5763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159971089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fde9c0d0b452a745fa63694337d7c60824f943ba0bc9628dca28dc4621035f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 12:41:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 15 May 2020 12:41:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 15 May 2020 12:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 12:41:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 May 2020 12:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 15 May 2020 12:49:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 15 May 2020 12:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 15 May 2020 12:49:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 15 May 2020 12:49:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 15 May 2020 12:49:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 May 2020 12:49:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 15 May 2020 14:23:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 15 May 2020 14:23:53 GMT
ENV PHP_VERSION=7.2.31
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Fri, 15 May 2020 14:23:54 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Fri, 15 May 2020 14:24:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 May 2020 14:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 15 May 2020 14:28:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 02 Jun 2020 21:27:21 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jun 2020 21:27:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 02 Jun 2020 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jun 2020 21:27:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jun 2020 21:27:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jun 2020 21:27:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:27:24 GMT
EXPOSE 80
# Tue, 02 Jun 2020 21:27:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jun 2020 21:56:00 GMT
RUN a2enmod rewrite
# Tue, 02 Jun 2020 21:57:36 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 02 Jun 2020 21:57:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_VERSION=1.13.2
# Tue, 02 Jun 2020 21:57:37 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Tue, 02 Jun 2020 21:57:40 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Tue, 02 Jun 2020 21:57:41 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 02 Jun 2020 21:57:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2020 21:57:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d895574014b07620962dc74d8e480e4629fbb3afb45c2bf57249a6ec1a0e64c`  
		Last Modified: Fri, 15 May 2020 15:07:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309fdad64103ed6195af8392df8834b3ba6c40ff2070a2230d835960c41e10b`  
		Last Modified: Fri, 15 May 2020 15:07:25 GMT  
		Size: 76.7 MB (76652092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c201f6a5d6f95f92d66f943b5413d3637ec1fce1735885558bca16f7302bfaed`  
		Last Modified: Fri, 15 May 2020 15:07:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f853892aac5282dcd651f71ce35d32c4f66c6c1e6864a13b10100dff4c1d5`  
		Last Modified: Fri, 15 May 2020 15:07:44 GMT  
		Size: 18.7 MB (18675995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998b2113b4005b0fc3cd483f8ec5e00202376f2b89a050cd742fc37627e40537`  
		Last Modified: Fri, 15 May 2020 15:07:41 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c0b4710d3bfd982a9a2fc845001e73b11043e83f3618713bbc5ed47218462c`  
		Last Modified: Fri, 15 May 2020 15:07:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e342cb20e11a1dd9d7c623fa9432bd079fde2b090476b3134baf0c21d40612a`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 12.6 MB (12648389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e1fe994da44df77bd8b6ad18ed428e3d1e7f76c83349d61cf8fa06beab4d`  
		Last Modified: Fri, 15 May 2020 15:11:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231d94c7c66658f89cc128cad35ec1e8e08f2bba42fd7ca4c2d1933d66910ac`  
		Last Modified: Fri, 15 May 2020 15:11:16 GMT  
		Size: 13.8 MB (13820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef45ec77068806c1e35a449069901a6954df90f88b07ea92c53a74d4a87181`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88824dfd94bf4cb4cbac4f54a87435f9f79999b2e5ddf6237e79a72e76345bb5`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56cee4a9e8f3c545a9583d5e54b1f5f9eec02031193cfd4ee7b375428d3c1e`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa9edfc095da1a62d22209cc50524637a488f110e3b576bb336ecc5763a5d6`  
		Last Modified: Tue, 02 Jun 2020 21:32:27 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590acb4319dde2c4114d57e04708f1dfaf8aaa664f9e942acb9ba9da1ac99474`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c045cc334cead04223ea03e50dd5654ffb2dfa1c21ce2961439b90dc50963ea`  
		Last Modified: Tue, 02 Jun 2020 21:59:37 GMT  
		Size: 2.6 MB (2600045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4aab25360ce839aae10ede75955379e159d51848af55379a5028a571cb0ddb`  
		Last Modified: Tue, 02 Jun 2020 21:59:39 GMT  
		Size: 8.5 MB (8468667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4dfd2fed81e1e25f8c50f3040f77a9b8384cab26a98c9bcc55fbee7a21e7d`  
		Last Modified: Tue, 02 Jun 2020 21:59:36 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:778bc416ca1ce2a36e963b9e578ef87b4ed24dc677f12add0381271b90103fbc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151980140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8232fd3ed566be17b50f4a2645b7391bfcd9cfbe83c6a6ecd25971125a9a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 10:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Jun 2020 10:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Jun 2020 10:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 10:23:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Jun 2020 10:23:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Jun 2020 10:27:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Jun 2020 10:28:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Jun 2020 10:28:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Jun 2020 10:28:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Jun 2020 10:28:24 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Jun 2020 10:28:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Jun 2020 10:28:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Jun 2020 10:28:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Jun 2020 11:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 09 Jun 2020 11:25:49 GMT
ENV PHP_VERSION=7.2.31
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.31.tar.xz.asc
# Tue, 09 Jun 2020 11:25:50 GMT
ENV PHP_SHA256=8beaa634bb878a96af9bc8643811ea46973f5f41ad2bfb6ab4cfd290e5a39806 PHP_MD5=
# Tue, 09 Jun 2020 11:26:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 09 Jun 2020 11:26:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 09 Jun 2020 11:29:11 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 09 Jun 2020 11:29:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 09 Jun 2020 11:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Jun 2020 11:29:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 11:29:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 09 Jun 2020 11:29:18 GMT
WORKDIR /var/www/html
# Tue, 09 Jun 2020 11:29:19 GMT
EXPOSE 80
# Tue, 09 Jun 2020 11:29:20 GMT
CMD ["apache2-foreground"]
# Wed, 10 Jun 2020 01:23:35 GMT
RUN a2enmod rewrite
# Wed, 10 Jun 2020 01:26:50 GMT
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 10 Jun 2020 01:26:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2020 01:26:53 GMT
ENV BACKDROP_VERSION=1.13.2
# Wed, 10 Jun 2020 01:26:54 GMT
ENV BACKDROP_MD5=c35ee388b82661b18ffacf87cb52aa2d
# Wed, 10 Jun 2020 01:27:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 10 Jun 2020 01:27:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 10 Jun 2020 01:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Jun 2020 01:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e42a0c192db5b0cb97d83007911b8069b7120ef4d150564a32e9ec94753ca03`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23edfc2b677695687c477af83edbcfb24140f7186ed405faef4d5947c0a0c9`  
		Last Modified: Tue, 09 Jun 2020 11:57:42 GMT  
		Size: 70.3 MB (70337397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22952435701f91bcb4b63b22ba1c37c84d3a2c0d2f3c98109e18618040b7bb32`  
		Last Modified: Tue, 09 Jun 2020 11:57:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4090b847c63cf622d705238850718bfaa914a66c26c09c72b4d9799d275f05`  
		Last Modified: Tue, 09 Jun 2020 11:58:10 GMT  
		Size: 18.6 MB (18579309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb37ac8c34eaa4fd0192c5f0d5fa5ba67a1be74bdb0715850f35818fad6ee35`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a637d0146b6020a2407694c81449ec07e33b411830a64f1b7bf3a652ec302adf`  
		Last Modified: Tue, 09 Jun 2020 11:58:05 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1198da107f32c37df51961a03cd97945cdd5481bef35493461cfe6df563bc65`  
		Last Modified: Tue, 09 Jun 2020 12:01:52 GMT  
		Size: 12.6 MB (12647088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6487c049a65d7cf238c48ae26721320aa0785247fb65cff0378a84ce5cd71d42`  
		Last Modified: Tue, 09 Jun 2020 12:01:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b9a240f67bd828560be64473521155b8e0c4f6307a6b36708e023ed7ee50db`  
		Last Modified: Tue, 09 Jun 2020 12:01:54 GMT  
		Size: 13.5 MB (13516996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ca3ae30b102493773014b9f4d9bb4e3de4ebdc48b62361271ee0df2dfc0320`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2432ebaa97fd265775752560e0f8f527bb917c2b3ba0654bcae9b36bc40ea66a`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c163e2adf86cd9e9090503d71d6ed65089155814aaf1b47cb8d0413b39f7b48`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c8fee54f098266796a7c7eff0a5e7ae920bf98d32cf27de7ff5854a7fa39b1`  
		Last Modified: Tue, 09 Jun 2020 12:01:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818da2ab6a6fc58792a03b5b1bd54317c00af5e7a3f5a6eeb5d8449526bc72e`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16735f68637b2060dcc043d4512241bc20beb9e11933458dec0cd0821196937`  
		Last Modified: Wed, 10 Jun 2020 01:31:23 GMT  
		Size: 2.6 MB (2565952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8f1dc1f05362e062ab997bb05f8fe9538d8bed2be497cc3ea795a04ac6709`  
		Last Modified: Wed, 10 Jun 2020 01:31:26 GMT  
		Size: 8.5 MB (8468808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b035b097e4a213a25576a7e8d098f1a67810480c53f944b58a4b6914383d391`  
		Last Modified: Wed, 10 Jun 2020 01:31:22 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
