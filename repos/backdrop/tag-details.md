<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.33`](#backdrop133)
-	[`backdrop:1.33-apache`](#backdrop133-apache)
-	[`backdrop:1.33-fpm`](#backdrop133-fpm)
-	[`backdrop:1.33.0`](#backdrop1330)
-	[`backdrop:1.33.0-apache`](#backdrop1330-apache)
-	[`backdrop:1.33.0-fpm`](#backdrop1330-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:54f851be5eda6c25e01a2b0b92d318f4d408996fa01d28cc73229023d268d343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:5413f5ff0bc6c9e5ce133d4670dbc5e490ab3d2a4e2b047469a16b17cb6ce115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188111092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5611bf3081c2c3c62be0aec78c4a158ce96524c10f2a8e0b47c72acb9f7a6956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:05:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:51 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:12:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:12:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:12:51 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:26:35 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:35 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:36 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:36 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb7071422ecd73d7df21a7467f66fcd3bb19f4dbc9328eaa86026a7e781f57`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee8432c63c855d453e3c52bd51b56bb2c3f7aa6922a9432fc050c7e3d79fb01`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 117.8 MB (117840596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd80f85f90e7677b1345e07c60dc5e1da24abc7847b2caf62356638e849f25b`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774d5ab71025fbc01b88ffa615c4597f6e5358fc77042396a49ceaa99f749d9`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 12.8 MB (12751397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febeee299a71e2f841db76884c29ff81b7e80f84eb37db2571a1aeb7b8990c62`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ca2663bd9de0c8c5d20a00d86e40d1fd1a207d5f586da68ac8ae21a3c4e5e4`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 11.9 MB (11902547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a31fba4c689cb4f45243b4d55ea4efc547a0f7dfebca554173402a4e6e3a4`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba60e194086d6759995cff306043ec9c7fd279f752b337d2c5a33dafd7c0e2`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4e565046b453afc97d48f1752bb9e13b18555518fc96488b8ac92a10c2204`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb9c09e66259ce8a30e447a2a298139d5e30283c8ba43569bf8a0ef5bd9ffc`  
		Last Modified: Tue, 19 May 2026 23:13:03 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33b661ab78253cc0baacb59e69fc54e33a9a5e78a2882cfb68f60bbe45391a`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.5 MB (6535653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2460b3540af0b365c819a61e9fdc5ec9b8976899ab4235f08d52f25b10f6c74`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2420734b1ce42b9be02195cc548e06c44e398047a2dcacffd027489d05a018`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c98e46cf2e6f7868c6d515cc09474e80b059fa0c927dbe82be136a50aac2ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f55f7b94437c50a9dcf2ef0b60cb16334b1544b3983697f84dc3a774b7f2a`

```dockerfile
```

-	Layers:
	-	`sha256:65852b6769a3948df3d9245cb183c771feda05dc6b1e4b04f9b86c8bb82c6b79`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.9 MB (6938177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044cf517507fcf2aea9463866134aa7dbe8dd17a9721bf4b42418327f9e94364`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:9e82bb46e605b16eb8fe986eb1249279f0d5cde0542960ab5c5e13a85edba7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181442001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01569083a08e59cc0297979be40dd6c57e4d52a5582f67d535f346a30689cd8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:07:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:14:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:14:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:14:40 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:14:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:14:40 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:14:40 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:27:58 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:27:58 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03d879ed4422e78acd0b2f35aff98a2f96243399f601155de182fe61a504e7`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f860689e58f365f3cbe2e7d063ef9d6406213cab5ade5dab0293b297ec38ca`  
		Last Modified: Tue, 19 May 2026 23:10:39 GMT  
		Size: 110.2 MB (110169226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be53f21933d0c1725dbb7414e3092f634db4a25e180731e235b326bcfe1388`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b41fa8de9f25b735bb742fbd5bbd6575f5cbf3ef44bc82cef50f5d08b0b9b34`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 12.8 MB (12750930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172998765ad9287cbf935a09721e91599d81b601c29a879050727fbeb22af5c9`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c515438e7422d251572d60e2355103d1b1f637f537b231d7797ea19f05ce96d`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 11.9 MB (11925410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4770d96c5c29c71593beb25b90edf58d16a9e7f73f4a2976e16df662bdbe87bf`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0826b2521779d94e34b4fea0d7aa6b5e16bd1420a897f37658a601c6a036dd21`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6c0bb237ba5fe948ebccf4f1a911f61bd623495547855fdf1916d27d98a49`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb498c8fd93b49ba046b89f16a3c4eec3b270683fa55e58f778909c7e66b832`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aaa80f9a2da47469db15de688a1240cedb95cb0e6730be53d03ad4eff728e3`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.2 MB (7153548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e03863c79710600fda2f7cc1af5c5a7358338ac90c54fcd75a5ca519ea9317`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 9.3 MB (9286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:17f5cad2178dcc65167ea0f5086d84748ea10a7e16fdce3a838e541b6fba3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b788bcf1b79ab885dc7f76f806f917c2400a1aec9d57a37b6b86798da05a674`

```dockerfile
```

-	Layers:
	-	`sha256:20c8036a41385dbc9e50543229986a70efbf1abec3557df630e4547bcf7cd1cf`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.0 MB (7035485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7803de99053e892c5135a0a000c220da7b6c9a869da08eb3c475f727a6e13848`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33-apache`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33-fpm`

```console
$ docker pull backdrop@sha256:54f851be5eda6c25e01a2b0b92d318f4d408996fa01d28cc73229023d268d343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:5413f5ff0bc6c9e5ce133d4670dbc5e490ab3d2a4e2b047469a16b17cb6ce115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188111092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5611bf3081c2c3c62be0aec78c4a158ce96524c10f2a8e0b47c72acb9f7a6956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:05:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:51 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:12:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:12:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:12:51 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:26:35 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:35 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:36 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:36 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb7071422ecd73d7df21a7467f66fcd3bb19f4dbc9328eaa86026a7e781f57`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee8432c63c855d453e3c52bd51b56bb2c3f7aa6922a9432fc050c7e3d79fb01`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 117.8 MB (117840596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd80f85f90e7677b1345e07c60dc5e1da24abc7847b2caf62356638e849f25b`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774d5ab71025fbc01b88ffa615c4597f6e5358fc77042396a49ceaa99f749d9`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 12.8 MB (12751397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febeee299a71e2f841db76884c29ff81b7e80f84eb37db2571a1aeb7b8990c62`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ca2663bd9de0c8c5d20a00d86e40d1fd1a207d5f586da68ac8ae21a3c4e5e4`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 11.9 MB (11902547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a31fba4c689cb4f45243b4d55ea4efc547a0f7dfebca554173402a4e6e3a4`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba60e194086d6759995cff306043ec9c7fd279f752b337d2c5a33dafd7c0e2`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4e565046b453afc97d48f1752bb9e13b18555518fc96488b8ac92a10c2204`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb9c09e66259ce8a30e447a2a298139d5e30283c8ba43569bf8a0ef5bd9ffc`  
		Last Modified: Tue, 19 May 2026 23:13:03 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33b661ab78253cc0baacb59e69fc54e33a9a5e78a2882cfb68f60bbe45391a`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.5 MB (6535653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2460b3540af0b365c819a61e9fdc5ec9b8976899ab4235f08d52f25b10f6c74`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2420734b1ce42b9be02195cc548e06c44e398047a2dcacffd027489d05a018`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c98e46cf2e6f7868c6d515cc09474e80b059fa0c927dbe82be136a50aac2ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f55f7b94437c50a9dcf2ef0b60cb16334b1544b3983697f84dc3a774b7f2a`

```dockerfile
```

-	Layers:
	-	`sha256:65852b6769a3948df3d9245cb183c771feda05dc6b1e4b04f9b86c8bb82c6b79`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.9 MB (6938177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044cf517507fcf2aea9463866134aa7dbe8dd17a9721bf4b42418327f9e94364`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:9e82bb46e605b16eb8fe986eb1249279f0d5cde0542960ab5c5e13a85edba7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181442001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01569083a08e59cc0297979be40dd6c57e4d52a5582f67d535f346a30689cd8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:07:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:14:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:14:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:14:40 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:14:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:14:40 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:14:40 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:27:58 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:27:58 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03d879ed4422e78acd0b2f35aff98a2f96243399f601155de182fe61a504e7`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f860689e58f365f3cbe2e7d063ef9d6406213cab5ade5dab0293b297ec38ca`  
		Last Modified: Tue, 19 May 2026 23:10:39 GMT  
		Size: 110.2 MB (110169226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be53f21933d0c1725dbb7414e3092f634db4a25e180731e235b326bcfe1388`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b41fa8de9f25b735bb742fbd5bbd6575f5cbf3ef44bc82cef50f5d08b0b9b34`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 12.8 MB (12750930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172998765ad9287cbf935a09721e91599d81b601c29a879050727fbeb22af5c9`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c515438e7422d251572d60e2355103d1b1f637f537b231d7797ea19f05ce96d`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 11.9 MB (11925410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4770d96c5c29c71593beb25b90edf58d16a9e7f73f4a2976e16df662bdbe87bf`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0826b2521779d94e34b4fea0d7aa6b5e16bd1420a897f37658a601c6a036dd21`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6c0bb237ba5fe948ebccf4f1a911f61bd623495547855fdf1916d27d98a49`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb498c8fd93b49ba046b89f16a3c4eec3b270683fa55e58f778909c7e66b832`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aaa80f9a2da47469db15de688a1240cedb95cb0e6730be53d03ad4eff728e3`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.2 MB (7153548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e03863c79710600fda2f7cc1af5c5a7358338ac90c54fcd75a5ca519ea9317`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 9.3 MB (9286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:17f5cad2178dcc65167ea0f5086d84748ea10a7e16fdce3a838e541b6fba3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b788bcf1b79ab885dc7f76f806f917c2400a1aec9d57a37b6b86798da05a674`

```dockerfile
```

-	Layers:
	-	`sha256:20c8036a41385dbc9e50543229986a70efbf1abec3557df630e4547bcf7cd1cf`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.0 MB (7035485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7803de99053e892c5135a0a000c220da7b6c9a869da08eb3c475f727a6e13848`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33.0`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33.0` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33.0` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33.0-apache`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33.0-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33.0-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.33.0-fpm`

```console
$ docker pull backdrop@sha256:54f851be5eda6c25e01a2b0b92d318f4d408996fa01d28cc73229023d268d343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.33.0-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:5413f5ff0bc6c9e5ce133d4670dbc5e490ab3d2a4e2b047469a16b17cb6ce115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188111092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5611bf3081c2c3c62be0aec78c4a158ce96524c10f2a8e0b47c72acb9f7a6956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:05:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:51 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:12:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:12:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:12:51 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:26:35 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:35 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:36 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:36 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb7071422ecd73d7df21a7467f66fcd3bb19f4dbc9328eaa86026a7e781f57`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee8432c63c855d453e3c52bd51b56bb2c3f7aa6922a9432fc050c7e3d79fb01`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 117.8 MB (117840596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd80f85f90e7677b1345e07c60dc5e1da24abc7847b2caf62356638e849f25b`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774d5ab71025fbc01b88ffa615c4597f6e5358fc77042396a49ceaa99f749d9`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 12.8 MB (12751397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febeee299a71e2f841db76884c29ff81b7e80f84eb37db2571a1aeb7b8990c62`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ca2663bd9de0c8c5d20a00d86e40d1fd1a207d5f586da68ac8ae21a3c4e5e4`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 11.9 MB (11902547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a31fba4c689cb4f45243b4d55ea4efc547a0f7dfebca554173402a4e6e3a4`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba60e194086d6759995cff306043ec9c7fd279f752b337d2c5a33dafd7c0e2`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4e565046b453afc97d48f1752bb9e13b18555518fc96488b8ac92a10c2204`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb9c09e66259ce8a30e447a2a298139d5e30283c8ba43569bf8a0ef5bd9ffc`  
		Last Modified: Tue, 19 May 2026 23:13:03 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33b661ab78253cc0baacb59e69fc54e33a9a5e78a2882cfb68f60bbe45391a`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.5 MB (6535653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2460b3540af0b365c819a61e9fdc5ec9b8976899ab4235f08d52f25b10f6c74`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2420734b1ce42b9be02195cc548e06c44e398047a2dcacffd027489d05a018`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c98e46cf2e6f7868c6d515cc09474e80b059fa0c927dbe82be136a50aac2ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f55f7b94437c50a9dcf2ef0b60cb16334b1544b3983697f84dc3a774b7f2a`

```dockerfile
```

-	Layers:
	-	`sha256:65852b6769a3948df3d9245cb183c771feda05dc6b1e4b04f9b86c8bb82c6b79`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.9 MB (6938177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044cf517507fcf2aea9463866134aa7dbe8dd17a9721bf4b42418327f9e94364`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.33.0-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:9e82bb46e605b16eb8fe986eb1249279f0d5cde0542960ab5c5e13a85edba7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181442001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01569083a08e59cc0297979be40dd6c57e4d52a5582f67d535f346a30689cd8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:07:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:14:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:14:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:14:40 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:14:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:14:40 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:14:40 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:27:58 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:27:58 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03d879ed4422e78acd0b2f35aff98a2f96243399f601155de182fe61a504e7`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f860689e58f365f3cbe2e7d063ef9d6406213cab5ade5dab0293b297ec38ca`  
		Last Modified: Tue, 19 May 2026 23:10:39 GMT  
		Size: 110.2 MB (110169226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be53f21933d0c1725dbb7414e3092f634db4a25e180731e235b326bcfe1388`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b41fa8de9f25b735bb742fbd5bbd6575f5cbf3ef44bc82cef50f5d08b0b9b34`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 12.8 MB (12750930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172998765ad9287cbf935a09721e91599d81b601c29a879050727fbeb22af5c9`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c515438e7422d251572d60e2355103d1b1f637f537b231d7797ea19f05ce96d`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 11.9 MB (11925410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4770d96c5c29c71593beb25b90edf58d16a9e7f73f4a2976e16df662bdbe87bf`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0826b2521779d94e34b4fea0d7aa6b5e16bd1420a897f37658a601c6a036dd21`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6c0bb237ba5fe948ebccf4f1a911f61bd623495547855fdf1916d27d98a49`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb498c8fd93b49ba046b89f16a3c4eec3b270683fa55e58f778909c7e66b832`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aaa80f9a2da47469db15de688a1240cedb95cb0e6730be53d03ad4eff728e3`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.2 MB (7153548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e03863c79710600fda2f7cc1af5c5a7358338ac90c54fcd75a5ca519ea9317`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 9.3 MB (9286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.33.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:17f5cad2178dcc65167ea0f5086d84748ea10a7e16fdce3a838e541b6fba3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b788bcf1b79ab885dc7f76f806f917c2400a1aec9d57a37b6b86798da05a674`

```dockerfile
```

-	Layers:
	-	`sha256:20c8036a41385dbc9e50543229986a70efbf1abec3557df630e4547bcf7cd1cf`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.0 MB (7035485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7803de99053e892c5135a0a000c220da7b6c9a869da08eb3c475f727a6e13848`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:54f851be5eda6c25e01a2b0b92d318f4d408996fa01d28cc73229023d268d343
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:5413f5ff0bc6c9e5ce133d4670dbc5e490ab3d2a4e2b047469a16b17cb6ce115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188111092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5611bf3081c2c3c62be0aec78c4a158ce96524c10f2a8e0b47c72acb9f7a6956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:05:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:06:14 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:51 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:12:51 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:12:51 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:12:51 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:26:35 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:35 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:36 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:36 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:36 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb7071422ecd73d7df21a7467f66fcd3bb19f4dbc9328eaa86026a7e781f57`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee8432c63c855d453e3c52bd51b56bb2c3f7aa6922a9432fc050c7e3d79fb01`  
		Last Modified: Tue, 19 May 2026 23:09:58 GMT  
		Size: 117.8 MB (117840596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd80f85f90e7677b1345e07c60dc5e1da24abc7847b2caf62356638e849f25b`  
		Last Modified: Tue, 19 May 2026 23:09:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774d5ab71025fbc01b88ffa615c4597f6e5358fc77042396a49ceaa99f749d9`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 12.8 MB (12751397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febeee299a71e2f841db76884c29ff81b7e80f84eb37db2571a1aeb7b8990c62`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ca2663bd9de0c8c5d20a00d86e40d1fd1a207d5f586da68ac8ae21a3c4e5e4`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 11.9 MB (11902547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a31fba4c689cb4f45243b4d55ea4efc547a0f7dfebca554173402a4e6e3a4`  
		Last Modified: Tue, 19 May 2026 23:13:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba60e194086d6759995cff306043ec9c7fd279f752b337d2c5a33dafd7c0e2`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4e565046b453afc97d48f1752bb9e13b18555518fc96488b8ac92a10c2204`  
		Last Modified: Tue, 19 May 2026 23:13:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadb9c09e66259ce8a30e447a2a298139d5e30283c8ba43569bf8a0ef5bd9ffc`  
		Last Modified: Tue, 19 May 2026 23:13:03 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba33b661ab78253cc0baacb59e69fc54e33a9a5e78a2882cfb68f60bbe45391a`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.5 MB (6535653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2460b3540af0b365c819a61e9fdc5ec9b8976899ab4235f08d52f25b10f6c74`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2420734b1ce42b9be02195cc548e06c44e398047a2dcacffd027489d05a018`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:c98e46cf2e6f7868c6d515cc09474e80b059fa0c927dbe82be136a50aac2ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f55f7b94437c50a9dcf2ef0b60cb16334b1544b3983697f84dc3a774b7f2a`

```dockerfile
```

-	Layers:
	-	`sha256:65852b6769a3948df3d9245cb183c771feda05dc6b1e4b04f9b86c8bb82c6b79`  
		Last Modified: Wed, 20 May 2026 00:26:49 GMT  
		Size: 6.9 MB (6938177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044cf517507fcf2aea9463866134aa7dbe8dd17a9721bf4b42418327f9e94364`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:9e82bb46e605b16eb8fe986eb1249279f0d5cde0542960ab5c5e13a85edba7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181442001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01569083a08e59cc0297979be40dd6c57e4d52a5582f67d535f346a30689cd8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:07:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:07:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:07:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:14:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:14:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:14:40 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:14:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:14:40 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:14:40 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:27:58 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:27:58 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:00 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03d879ed4422e78acd0b2f35aff98a2f96243399f601155de182fe61a504e7`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f860689e58f365f3cbe2e7d063ef9d6406213cab5ade5dab0293b297ec38ca`  
		Last Modified: Tue, 19 May 2026 23:10:39 GMT  
		Size: 110.2 MB (110169226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be53f21933d0c1725dbb7414e3092f634db4a25e180731e235b326bcfe1388`  
		Last Modified: Tue, 19 May 2026 23:10:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b41fa8de9f25b735bb742fbd5bbd6575f5cbf3ef44bc82cef50f5d08b0b9b34`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 12.8 MB (12750930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172998765ad9287cbf935a09721e91599d81b601c29a879050727fbeb22af5c9`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c515438e7422d251572d60e2355103d1b1f637f537b231d7797ea19f05ce96d`  
		Last Modified: Tue, 19 May 2026 23:14:52 GMT  
		Size: 11.9 MB (11925410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4770d96c5c29c71593beb25b90edf58d16a9e7f73f4a2976e16df662bdbe87bf`  
		Last Modified: Tue, 19 May 2026 23:14:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0826b2521779d94e34b4fea0d7aa6b5e16bd1420a897f37658a601c6a036dd21`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c6c0bb237ba5fe948ebccf4f1a911f61bd623495547855fdf1916d27d98a49`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb498c8fd93b49ba046b89f16a3c4eec3b270683fa55e58f778909c7e66b832`  
		Last Modified: Tue, 19 May 2026 23:14:53 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aaa80f9a2da47469db15de688a1240cedb95cb0e6730be53d03ad4eff728e3`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.2 MB (7153548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e03863c79710600fda2f7cc1af5c5a7358338ac90c54fcd75a5ca519ea9317`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 9.3 MB (9286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:17f5cad2178dcc65167ea0f5086d84748ea10a7e16fdce3a838e541b6fba3d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b788bcf1b79ab885dc7f76f806f917c2400a1aec9d57a37b6b86798da05a674`

```dockerfile
```

-	Layers:
	-	`sha256:20c8036a41385dbc9e50543229986a70efbf1abec3557df630e4547bcf7cd1cf`  
		Last Modified: Wed, 20 May 2026 00:28:13 GMT  
		Size: 7.0 MB (7035485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7803de99053e892c5135a0a000c220da7b6c9a869da08eb3c475f727a6e13848`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:c357856ce9759a7c92b095b557c02e5c6e88a735b96c6b01e4c655881c7f94d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:64176f0466078718440c4d59be5f69ce751f3e4cf991018c1639da4117e750b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192160023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df72aa094013548aac556c4b8e8d85226d4e1219d4618f40755b7cffcf5a6c7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:06:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:10:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:10:09 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:12:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:12:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:25:39 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:26:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:26:22 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:26:24 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:26:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:26:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:26:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81875e03a86e4d663a578b57136a6dde52b1f3f617c06a340688b5b53f81720`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa392ebbb80c0466c93d5892fb4a3884563f6ab46bf66de2cae60677f1ff219`  
		Last Modified: Tue, 19 May 2026 23:09:49 GMT  
		Size: 117.8 MB (117840531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11284aac47a9af86f6d60cad8304115b15bfb6d1dc09a8416bd48f5ba97896`  
		Last Modified: Tue, 19 May 2026 23:09:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f3a4740909ef0e323a8541d2a8802c4f1a0ebdce9bd6b9370545ebd3a38b4`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 4.2 MB (4227830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf5064b55f1d48dcbd0468ce453f418d83ee94ec606d96fc7450968532a04ba`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd9b27175b2019cedb24a0408b5ba87a96e5407025026066bbbbb0251edf98`  
		Last Modified: Tue, 19 May 2026 23:12:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9fd1693439f5a85c9b91f6528eae79bb03fc6119f744a8f47c130ba4a9dd`  
		Last Modified: Tue, 19 May 2026 23:12:55 GMT  
		Size: 12.8 MB (12770098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca30975eae49df39cfca47a867f688951a094f3e592165cbb70950e8e4d3d28`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320d77ecabde025c3e52e281473b0426c5b343d3d46c7f59a2a9fd1317d24f6d`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 11.7 MB (11715369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa05b5032b13a4aad76560c08aaa55202838605d1d4f2d0b22f0a783da5d270e`  
		Last Modified: Tue, 19 May 2026 23:12:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233764c9d8b3f42a129b45fdb33e1f3182ebdd100e4ab18bcb6cbfa7ea43d58`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a376359321f9c3d84c1864b3c375157c39a8c0870b3b04490c1ffc839c8fde`  
		Last Modified: Tue, 19 May 2026 23:12:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862ee81cb220aeaef6d33d5dd1f5be0378b25d60b1516f10ab6cc9240855ed69`  
		Last Modified: Tue, 19 May 2026 23:12:58 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199c573e28822261d6d9095932b50377c646d67554013e3d0b3f2513140768a`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 306.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007c32ee4332b72e57c5848f9146b89370feb047fbfcfc5b080a6d67cf89db6`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 6.5 MB (6532434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bb32a8ee4f58b0910f373d56dfe32ba183779d3ada0ccd4082bac9c38532b1`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 9.3 MB (9286815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a346c3a27ac1f20aa4193f8920379cc467384a043946e0e0c2ac012821c7d8`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:a3d180d18e44490ad4e4e24367a98da2dfa052bbd4daf8218926c762c4e5965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a898a82670a8b2760c413028af4a0cd03596b14658f0992f28b29e43528795e6`

```dockerfile
```

-	Layers:
	-	`sha256:937675c43975b50f121d4e7b121d7c812f4707a3037392c1a4cdafb528b8fd85`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 7.5 MB (7461778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bfba1cee7e57d19c9ec1453be209bc097c2e40b0af77894fe1036230388e40`  
		Last Modified: Wed, 20 May 2026 00:26:37 GMT  
		Size: 30.6 KB (30558 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:09de9f667fdc621f0372c3938dd349dce0c27caa954f5d04a52e855264becf7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185570639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8777d03c461c303ebfd69659e4546d201a52213d73e4cac900c8390bc42d06f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:10:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:11:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:11:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:11:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:11:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:11:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 19 May 2026 23:11:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 19 May 2026 23:11:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:11:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:16 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:16 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:26:53 GMT
RUN a2enmod rewrite # buildkit
# Wed, 20 May 2026 00:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Wed, 20 May 2026 00:28:02 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_VERSION=1.33.0
# Wed, 20 May 2026 00:28:04 GMT
ENV BACKDROP_MD5=9b5e3fb6ac833e2adc2857f050d3f143
# Wed, 20 May 2026 00:28:04 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Wed, 20 May 2026 00:28:04 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:28:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:28:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9bc07105a98abf9359901ea46e9995c38bb750d553ad7b5ed6e6ec8a4d7e7c`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40274e600ddabb730115b7fa413000d3c44ad13020c0e210b251592c1e70e1ef`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 110.2 MB (110169473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea39d59b51cf2089e94a759ca333ba518fdb1cd9a7aa559b41708ed994d4c13`  
		Last Modified: Tue, 19 May 2026 23:15:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9cd3261664a3106cbe7437e7bd5666d4259b5fab2b9def1322579b4bdca44`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 4.3 MB (4307912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f7800c15a2fe28587a0812c76bd5157f323c965101d7d36d5bfd9db499469`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b92c395e964e202d11ed0ef3d11d89f4ff8557d78080728b4a57c0af3b0f70e`  
		Last Modified: Tue, 19 May 2026 23:15:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33aaef821230d455ef3a41883bd46b35492e00bd18865cc3261ad1011f908e`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 12.8 MB (12769696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeaf2a0d865476d3c9e5af08aee288f897cc2ffc0897e7e574f2d4da1e8a12b`  
		Last Modified: Tue, 19 May 2026 23:15:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dda7febf0cfcc7831f17e0e7d091dbad7d90237d9012753c7c8f7640909375`  
		Last Modified: Tue, 19 May 2026 23:15:43 GMT  
		Size: 11.7 MB (11734662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f66f0b165b37038d149fa9c13244b52061ac81b6e3d8805d5937cbe6c146d3d`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf69b070ae88882405a53f2096fdb85c0db2c5fb444cd4e46475a597549d66`  
		Last Modified: Tue, 19 May 2026 23:15:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5a013ab84f5002005874317814be677e7a76f3d084c3be72d9b305a18c0c0`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab430b9162244171500f365503ffd6f93c8f7d52a2be3f0627656aeb73cda38f`  
		Last Modified: Tue, 19 May 2026 23:15:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce0b9b9305736aee3a6ab39a853e70cb4903e93cf7d5af576a490266ba52a8e`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6737a7b12a2e1829821daef1905b8517414bdcd6789a7d49bb221004bc77560d`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.2 MB (7153141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d109201c6e43e5f5f621933fcf9e149921f553aa363f27654e77feaeb19e1`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 9.3 MB (9286807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e58b2526e46e8c843d0e13a182adf861e7bb2cee9b96c8c28464ac4f17ea2`  
		Last Modified: Wed, 20 May 2026 00:28:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:bb6e2ebca0f6bc3071dbcc48e7aeedaca25f25b70fda9bf8820cfba63badbd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc166203a88e82aab9912739d64c5389bb31419b118588e7155c73ccd4cfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:a2e28dc3fede500a41f84ab13011e5c69ec5ee6b793ffbef36da1e361903d64f`  
		Last Modified: Wed, 20 May 2026 00:28:17 GMT  
		Size: 7.6 MB (7559150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e59791a8f86d78dba3080938655c4d045c6d5f1e634f0e11f18df44bf06fc5b`  
		Last Modified: Wed, 20 May 2026 00:28:16 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json
