<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.31`](#backdrop131)
-	[`backdrop:1.31-apache`](#backdrop131-apache)
-	[`backdrop:1.31-fpm`](#backdrop131-fpm)
-	[`backdrop:1.31.0`](#backdrop1310)
-	[`backdrop:1.31.0-apache`](#backdrop1310-apache)
-	[`backdrop:1.31.0-fpm`](#backdrop1310-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:baaf0b0745214bfb66d5d20d3701b44934a06d6507cc99b4169894c067c302a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a1d5e634156cd513286a8e485138c1e7ca7e31f39c3ab078e6a33df21c7839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187598812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d4f1e3d9e44a4fb858b6132adee51714324e892a2ec5cc9cb56f8594f49f8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8508b1f217bbb2560830dd12c2a2995d1a0f1916ec66d2e8e7fc842e70ab46`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeeecc41c9a788cd5a18e4ec44256f769c612428a2073c6652a82ab02c1a559`  
		Last Modified: Thu, 03 Jul 2025 23:03:41 GMT  
		Size: 104.3 MB (104331379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec14772bf841e9591c3fd49d61c8ec886fffc5ea2587ea5b1d0c927796f825`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 12.7 MB (12687490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082345387e0e047ffcc42b66b2c813b215835ac08c08e67474a8fcbaa65b2ec`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9668880facffe40d0c21cdfc42a7dfebb945ab68544147f57d77300a4e002`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 27.8 MB (27827689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009fd29da09c1a58c29365476d6bf0b0b74d03898c9f5cc94cf8e1207110ae`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c210824a2f1d29785019f87e2f18b65aabb157c8546094264d4eb6441786bd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f57d5cfefa1dccf4a3cdfba73759d909c5a351bacd670990f1b49c1e2b859d`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958851e84b268638be7f47daedc49341755c74453a9948255a55918ebfd1d288`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2332eeafe0bdc565a774dd23acf2c6751a124c0508c63407a489d02a77183`  
		Last Modified: Thu, 03 Jul 2025 23:13:15 GMT  
		Size: 5.6 MB (5589700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f8cf87dff2155326ea51be2b27961ecbf8e01f6e86ec20fa4c9cfe44f0ca7`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 8.9 MB (8918328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511a9eb766fb3a87f2e673d4c4f8a334e5cffd3bfd80744905ddd12569c1992`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c90e4704dba55ea7d3efdb2314d130d76f8e911e5aa59c01d78e50ffe3054dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e42a5961c52f34551e06fc70814aa5e36bfdb828a3c37815cb176bf5333e75`

```dockerfile
```

-	Layers:
	-	`sha256:a41494b225f743c879f45141633d53c12b1baca687f60b214056ede9678ee1e6`  
		Last Modified: Fri, 04 Jul 2025 00:26:27 GMT  
		Size: 6.6 MB (6622355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86612b680f1330cbab566e605fd79873611d79691c48b2de99525afabbe10d8d`  
		Last Modified: Fri, 04 Jul 2025 00:26:28 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:6f029d485bfb597f48d7c709e6a93e854ff9599450b8765b8967b66164d60aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181227880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd147b5b64b2377c94be1a797fececba9bfe788917cae095524fda2d04024d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c2fe8af0108e02280aac7dd04598fb54e836a414297d9830f687e556a5397`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 5.6 MB (5606888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61268fdd8c9462bbb5e85f62cc682d3d7106a0f5644d8c24e31cf26d3f12431d`  
		Last Modified: Tue, 01 Jul 2025 13:28:19 GMT  
		Size: 8.9 MB (8918331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03d9832840959e1df77c66d51b453eb58babbae0b5288b6e9376bb01c98c06`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:0909949ded6de2a31a2ed029097194b6ed83486e10941c34bdf3a8c9c241192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ae5193604ff4ac516baf6b3ed8bd664bb4b945bfd52837256ec4f3093b2794`

```dockerfile
```

-	Layers:
	-	`sha256:4f166664594ddd405c239051263425b2fbb0a59788202e955938daa5b73af23d`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 6.7 MB (6650772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db6ef933cadf81a5601ffc50daefdd824099ec586335cf4ccfe6e27c69acae1`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 22.5 KB (22468 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31-apache`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31-fpm`

```console
$ docker pull backdrop@sha256:baaf0b0745214bfb66d5d20d3701b44934a06d6507cc99b4169894c067c302a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a1d5e634156cd513286a8e485138c1e7ca7e31f39c3ab078e6a33df21c7839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187598812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d4f1e3d9e44a4fb858b6132adee51714324e892a2ec5cc9cb56f8594f49f8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8508b1f217bbb2560830dd12c2a2995d1a0f1916ec66d2e8e7fc842e70ab46`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeeecc41c9a788cd5a18e4ec44256f769c612428a2073c6652a82ab02c1a559`  
		Last Modified: Thu, 03 Jul 2025 23:03:41 GMT  
		Size: 104.3 MB (104331379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec14772bf841e9591c3fd49d61c8ec886fffc5ea2587ea5b1d0c927796f825`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 12.7 MB (12687490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082345387e0e047ffcc42b66b2c813b215835ac08c08e67474a8fcbaa65b2ec`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9668880facffe40d0c21cdfc42a7dfebb945ab68544147f57d77300a4e002`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 27.8 MB (27827689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009fd29da09c1a58c29365476d6bf0b0b74d03898c9f5cc94cf8e1207110ae`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c210824a2f1d29785019f87e2f18b65aabb157c8546094264d4eb6441786bd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f57d5cfefa1dccf4a3cdfba73759d909c5a351bacd670990f1b49c1e2b859d`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958851e84b268638be7f47daedc49341755c74453a9948255a55918ebfd1d288`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2332eeafe0bdc565a774dd23acf2c6751a124c0508c63407a489d02a77183`  
		Last Modified: Thu, 03 Jul 2025 23:13:15 GMT  
		Size: 5.6 MB (5589700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f8cf87dff2155326ea51be2b27961ecbf8e01f6e86ec20fa4c9cfe44f0ca7`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 8.9 MB (8918328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511a9eb766fb3a87f2e673d4c4f8a334e5cffd3bfd80744905ddd12569c1992`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c90e4704dba55ea7d3efdb2314d130d76f8e911e5aa59c01d78e50ffe3054dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e42a5961c52f34551e06fc70814aa5e36bfdb828a3c37815cb176bf5333e75`

```dockerfile
```

-	Layers:
	-	`sha256:a41494b225f743c879f45141633d53c12b1baca687f60b214056ede9678ee1e6`  
		Last Modified: Fri, 04 Jul 2025 00:26:27 GMT  
		Size: 6.6 MB (6622355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86612b680f1330cbab566e605fd79873611d79691c48b2de99525afabbe10d8d`  
		Last Modified: Fri, 04 Jul 2025 00:26:28 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:6f029d485bfb597f48d7c709e6a93e854ff9599450b8765b8967b66164d60aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181227880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd147b5b64b2377c94be1a797fececba9bfe788917cae095524fda2d04024d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c2fe8af0108e02280aac7dd04598fb54e836a414297d9830f687e556a5397`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 5.6 MB (5606888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61268fdd8c9462bbb5e85f62cc682d3d7106a0f5644d8c24e31cf26d3f12431d`  
		Last Modified: Tue, 01 Jul 2025 13:28:19 GMT  
		Size: 8.9 MB (8918331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03d9832840959e1df77c66d51b453eb58babbae0b5288b6e9376bb01c98c06`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:0909949ded6de2a31a2ed029097194b6ed83486e10941c34bdf3a8c9c241192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ae5193604ff4ac516baf6b3ed8bd664bb4b945bfd52837256ec4f3093b2794`

```dockerfile
```

-	Layers:
	-	`sha256:4f166664594ddd405c239051263425b2fbb0a59788202e955938daa5b73af23d`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 6.7 MB (6650772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db6ef933cadf81a5601ffc50daefdd824099ec586335cf4ccfe6e27c69acae1`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 22.5 KB (22468 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31.0`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31.0` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31.0` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31.0-apache`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31.0-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31.0-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.31.0-fpm`

```console
$ docker pull backdrop@sha256:baaf0b0745214bfb66d5d20d3701b44934a06d6507cc99b4169894c067c302a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.31.0-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a1d5e634156cd513286a8e485138c1e7ca7e31f39c3ab078e6a33df21c7839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187598812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d4f1e3d9e44a4fb858b6132adee51714324e892a2ec5cc9cb56f8594f49f8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8508b1f217bbb2560830dd12c2a2995d1a0f1916ec66d2e8e7fc842e70ab46`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeeecc41c9a788cd5a18e4ec44256f769c612428a2073c6652a82ab02c1a559`  
		Last Modified: Thu, 03 Jul 2025 23:03:41 GMT  
		Size: 104.3 MB (104331379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec14772bf841e9591c3fd49d61c8ec886fffc5ea2587ea5b1d0c927796f825`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 12.7 MB (12687490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082345387e0e047ffcc42b66b2c813b215835ac08c08e67474a8fcbaa65b2ec`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9668880facffe40d0c21cdfc42a7dfebb945ab68544147f57d77300a4e002`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 27.8 MB (27827689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009fd29da09c1a58c29365476d6bf0b0b74d03898c9f5cc94cf8e1207110ae`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c210824a2f1d29785019f87e2f18b65aabb157c8546094264d4eb6441786bd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f57d5cfefa1dccf4a3cdfba73759d909c5a351bacd670990f1b49c1e2b859d`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958851e84b268638be7f47daedc49341755c74453a9948255a55918ebfd1d288`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2332eeafe0bdc565a774dd23acf2c6751a124c0508c63407a489d02a77183`  
		Last Modified: Thu, 03 Jul 2025 23:13:15 GMT  
		Size: 5.6 MB (5589700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f8cf87dff2155326ea51be2b27961ecbf8e01f6e86ec20fa4c9cfe44f0ca7`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 8.9 MB (8918328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511a9eb766fb3a87f2e673d4c4f8a334e5cffd3bfd80744905ddd12569c1992`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c90e4704dba55ea7d3efdb2314d130d76f8e911e5aa59c01d78e50ffe3054dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e42a5961c52f34551e06fc70814aa5e36bfdb828a3c37815cb176bf5333e75`

```dockerfile
```

-	Layers:
	-	`sha256:a41494b225f743c879f45141633d53c12b1baca687f60b214056ede9678ee1e6`  
		Last Modified: Fri, 04 Jul 2025 00:26:27 GMT  
		Size: 6.6 MB (6622355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86612b680f1330cbab566e605fd79873611d79691c48b2de99525afabbe10d8d`  
		Last Modified: Fri, 04 Jul 2025 00:26:28 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.31.0-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:6f029d485bfb597f48d7c709e6a93e854ff9599450b8765b8967b66164d60aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181227880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd147b5b64b2377c94be1a797fececba9bfe788917cae095524fda2d04024d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c2fe8af0108e02280aac7dd04598fb54e836a414297d9830f687e556a5397`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 5.6 MB (5606888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61268fdd8c9462bbb5e85f62cc682d3d7106a0f5644d8c24e31cf26d3f12431d`  
		Last Modified: Tue, 01 Jul 2025 13:28:19 GMT  
		Size: 8.9 MB (8918331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03d9832840959e1df77c66d51b453eb58babbae0b5288b6e9376bb01c98c06`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.31.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:0909949ded6de2a31a2ed029097194b6ed83486e10941c34bdf3a8c9c241192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ae5193604ff4ac516baf6b3ed8bd664bb4b945bfd52837256ec4f3093b2794`

```dockerfile
```

-	Layers:
	-	`sha256:4f166664594ddd405c239051263425b2fbb0a59788202e955938daa5b73af23d`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 6.7 MB (6650772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db6ef933cadf81a5601ffc50daefdd824099ec586335cf4ccfe6e27c69acae1`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 22.5 KB (22468 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:baaf0b0745214bfb66d5d20d3701b44934a06d6507cc99b4169894c067c302a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0a1d5e634156cd513286a8e485138c1e7ca7e31f39c3ab078e6a33df21c7839d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187598812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d4f1e3d9e44a4fb858b6132adee51714324e892a2ec5cc9cb56f8594f49f8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8508b1f217bbb2560830dd12c2a2995d1a0f1916ec66d2e8e7fc842e70ab46`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeeecc41c9a788cd5a18e4ec44256f769c612428a2073c6652a82ab02c1a559`  
		Last Modified: Thu, 03 Jul 2025 23:03:41 GMT  
		Size: 104.3 MB (104331379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec14772bf841e9591c3fd49d61c8ec886fffc5ea2587ea5b1d0c927796f825`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 12.7 MB (12687490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082345387e0e047ffcc42b66b2c813b215835ac08c08e67474a8fcbaa65b2ec`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9668880facffe40d0c21cdfc42a7dfebb945ab68544147f57d77300a4e002`  
		Last Modified: Thu, 03 Jul 2025 23:03:34 GMT  
		Size: 27.8 MB (27827689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01009fd29da09c1a58c29365476d6bf0b0b74d03898c9f5cc94cf8e1207110ae`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c210824a2f1d29785019f87e2f18b65aabb157c8546094264d4eb6441786bd3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f57d5cfefa1dccf4a3cdfba73759d909c5a351bacd670990f1b49c1e2b859d`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958851e84b268638be7f47daedc49341755c74453a9948255a55918ebfd1d288`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2332eeafe0bdc565a774dd23acf2c6751a124c0508c63407a489d02a77183`  
		Last Modified: Thu, 03 Jul 2025 23:13:15 GMT  
		Size: 5.6 MB (5589700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f8cf87dff2155326ea51be2b27961ecbf8e01f6e86ec20fa4c9cfe44f0ca7`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 8.9 MB (8918328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4511a9eb766fb3a87f2e673d4c4f8a334e5cffd3bfd80744905ddd12569c1992`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c90e4704dba55ea7d3efdb2314d130d76f8e911e5aa59c01d78e50ffe3054dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e42a5961c52f34551e06fc70814aa5e36bfdb828a3c37815cb176bf5333e75`

```dockerfile
```

-	Layers:
	-	`sha256:a41494b225f743c879f45141633d53c12b1baca687f60b214056ede9678ee1e6`  
		Last Modified: Fri, 04 Jul 2025 00:26:27 GMT  
		Size: 6.6 MB (6622355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86612b680f1330cbab566e605fd79873611d79691c48b2de99525afabbe10d8d`  
		Last Modified: Fri, 04 Jul 2025 00:26:28 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:6f029d485bfb597f48d7c709e6a93e854ff9599450b8765b8967b66164d60aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181227880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fd147b5b64b2377c94be1a797fececba9bfe788917cae095524fda2d04024d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c2fe8af0108e02280aac7dd04598fb54e836a414297d9830f687e556a5397`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 5.6 MB (5606888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61268fdd8c9462bbb5e85f62cc682d3d7106a0f5644d8c24e31cf26d3f12431d`  
		Last Modified: Tue, 01 Jul 2025 13:28:19 GMT  
		Size: 8.9 MB (8918331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03d9832840959e1df77c66d51b453eb58babbae0b5288b6e9376bb01c98c06`  
		Last Modified: Tue, 01 Jul 2025 13:28:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:0909949ded6de2a31a2ed029097194b6ed83486e10941c34bdf3a8c9c241192c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ae5193604ff4ac516baf6b3ed8bd664bb4b945bfd52837256ec4f3093b2794`

```dockerfile
```

-	Layers:
	-	`sha256:4f166664594ddd405c239051263425b2fbb0a59788202e955938daa5b73af23d`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 6.7 MB (6650772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db6ef933cadf81a5601ffc50daefdd824099ec586335cf4ccfe6e27c69acae1`  
		Last Modified: Tue, 01 Jul 2025 15:26:32 GMT  
		Size: 22.5 KB (22468 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:a38ee4ad50d413725ff1f800ad413c63c7ba2a959a1a025ee75ddfaa1609e9da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:60b9941c3fc64c3e865eb50f67ba3272cb9dd6d1de4de22998a68b378c6d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191560065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb99de9a8acf73ad33118cd0afc181184e3e95020a30c9636ab7190c450173d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.23
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e919a2ca2b5d31ba03208300997de14b3285b6af333c397e7708abb2801e74`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 304.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659b45732bc14be13bf76b022d3c1d4dbfb5dbba830ada4f4c2e337f3d3c69`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 5.6 MB (5584477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9c58f36cf41501e03af089b7ff991c6b7aafd9aab7a0368e0ee93c83d6a4c6`  
		Last Modified: Thu, 03 Jul 2025 23:13:18 GMT  
		Size: 8.9 MB (8918319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26375f807384d6c55a94f2a0c69dcfdec6348699f7019c8145be624a3f4a1`  
		Last Modified: Thu, 03 Jul 2025 23:13:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:9003bc8fbf9d5b255ef4c8b27583fc072f564d4cd44354060af1c51b5aec0bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7175758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f863c23df0c6519b6f59f2f4f0b41ee55843a9e8c0711dc0bb1b5b6d34be6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fccb01a7d96c6a4bab67739adc3c3bd9499144e945f7c1d72791f70659318d`  
		Last Modified: Fri, 04 Jul 2025 00:26:22 GMT  
		Size: 7.1 MB (7145151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80833acd9092daa078370ec4523c9cc6c331256cdcc5619e9e61548ad9d2e285`  
		Last Modified: Fri, 04 Jul 2025 00:26:23 GMT  
		Size: 30.6 KB (30607 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:86c1ad68c727bf4045609b713615b68eb82fdb435b8e8032289f1859755aae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185235538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f365749cb6fb307417cd775522739baf02928075a09a47dec16d5e7e9f6c75a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 16 May 2025 15:29:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.22
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 May 2025 15:29:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[80/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
# Fri, 16 May 2025 15:29:55 GMT
RUN a2enmod rewrite # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0338344fbbdf3fd875b6282992d879c84330f79444f2b26fa06fd262d91f5b66`  
		Last Modified: Tue, 01 Jul 2025 03:19:33 GMT  
		Size: 20.1 MB (20136183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6599ba91eea05ea5485c293321ec9fb98775e592c2b807fb3728dd999380d`  
		Last Modified: Tue, 01 Jul 2025 03:19:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38126f76137940856be8dca967826d804d2ea33b4661b247ce1768d9a21aed1`  
		Last Modified: Tue, 01 Jul 2025 03:19:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ecc6beb1a96003f7c47d08461c737346f6bac68cc5204c24fca6089f9b92f`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 12.7 MB (12683485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a275a9082e578200d65cd75cc7ebe68edcc53a66e4d90dd03ce66cf69aa55da0`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c57c613f19ee3c58e0192fe5f73f5678baaec1b99c00b70396422d361d87eb`  
		Last Modified: Tue, 01 Jul 2025 04:44:54 GMT  
		Size: 11.7 MB (11680169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e519875501133ecb60ce7f5d9fe01cea2349f851028ef25b24459edf4c6d0cb3`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f255c5e61d138a7af39389d9b358e61a69ecb5b437c5abaf525ee40e14fb295`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5819db2a66775ea77adcbcab381af2ee0a4a2f945ce7f5f51dba9348d3c66a84`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f184db4b4081e53c187556d71caceb25928d88323ca40bbd42870b6289b1a5`  
		Last Modified: Tue, 01 Jul 2025 04:44:53 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd50c1e5398b926b5646a8f037c86fb33948e0c7f6eaacb03a86d3ef815dbc1`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40159e64013b924bde7dd8a32a13983c63b758106c50139b328e9041d9e04b54`  
		Last Modified: Tue, 01 Jul 2025 13:26:44 GMT  
		Size: 5.6 MB (5602010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb881ff21e7954b905cfa4c571b3eeda8f4141818317e026968a54eee752be`  
		Last Modified: Tue, 01 Jul 2025 13:26:46 GMT  
		Size: 8.9 MB (8918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b89fcde6f1b542962fe7a4a45473d77c1942953e4407687a73e7294b13585c`  
		Last Modified: Tue, 01 Jul 2025 13:26:42 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:553689c0d6f182a4a980b2d7cf4f7a361ece88170db2a7ed206b7c0094ad9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0adf5787c6f57499645d3170a834f90543d848c9f887c9e997d2519a533ad`

```dockerfile
```

-	Layers:
	-	`sha256:ed7d7b714893c5026c9ddf39ecad4fa643c2d9577ca0c54e47b5e892f3d90bd3`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 7.2 MB (7173632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54ecbda2bf1e8e1e8f89b58c30ad1aa0f2adbee8515d656b58e407f0523c877`  
		Last Modified: Tue, 01 Jul 2025 15:26:26 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
