## `drupal:rc-php8.2-apache-bullseye`

```console
$ docker pull drupal@sha256:9b2d7dacce9357edd3a3aaa3d828ef6b1162f813ce8058e2c2be1ffbcdd5b4f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
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

### `drupal:rc-php8.2-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:a45baf61e25467b8dcf78a2362147999609cba6df53e353dfc93f417ec00c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188014245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc85ee4c3442d466299119fa55e28b907563a225c6e0ff717a3e37f3f47f3c7a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda1c0dfa3d207c7345cdb409f0201d824fb91ca69bcfc25aefe89fe932ab69`  
		Last Modified: Tue, 23 Jul 2024 09:37:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39638e336db23af0b7f959d4b99488f062382f53cc5790fcfdcf1a0ec5c3e4e`  
		Last Modified: Tue, 23 Jul 2024 09:37:15 GMT  
		Size: 91.6 MB (91646812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ec6db491a2507801e58c6651821fee426ae42f6ce0f8f5e3b949d68923ed33`  
		Last Modified: Tue, 23 Jul 2024 09:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b351a174415b7671a027b5c634fee0c73e0321eca6402f2c8f957a760962a0c6`  
		Last Modified: Tue, 23 Jul 2024 09:37:31 GMT  
		Size: 19.3 MB (19279178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77048257c4cae5dc30e837ff1110c11eb053408b952c9f6307699ff324ade8b2`  
		Last Modified: Tue, 23 Jul 2024 09:37:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf3d571ec001efa2ea92350b1a448b0709b88e62889c5f944036b3bcd6ad3`  
		Last Modified: Tue, 23 Jul 2024 09:37:28 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35be38363a498eff8887072b54b4175ec7f44387de6e99a7029cb6d20b43349a`  
		Last Modified: Tue, 23 Jul 2024 09:47:20 GMT  
		Size: 12.4 MB (12447124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc37f1185951271eae0675f0d43db3c96f136235f290bdb90bc6b24886fd177`  
		Last Modified: Tue, 23 Jul 2024 09:47:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba32a8d8a83f9094b37463ef264cdd4988957b0be65d8620a2125c990f63dcf`  
		Last Modified: Tue, 23 Jul 2024 09:47:20 GMT  
		Size: 11.3 MB (11342360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3544078a07e872a969dfd30a9d548982933e81b3909cab946102b587df724137`  
		Last Modified: Tue, 23 Jul 2024 09:47:18 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16263a03d7da84ff51e58899a138d3917bdbce679d99d3bcaf9814c1bd8fdd3b`  
		Last Modified: Tue, 23 Jul 2024 09:47:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32565e394ea4dfa5712c682f0995b7ed1e967a2770ee4a6b564022c5656738`  
		Last Modified: Tue, 23 Jul 2024 09:47:18 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de8f40c045412332001ae2ad319d5ee6ff859646bcf1dc884537c099ccb8fc6`  
		Last Modified: Tue, 23 Jul 2024 11:10:11 GMT  
		Size: 1.9 MB (1928473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c0c1d37101f5088cfcf73bd5ec4449025026156c6e7a6345af19d7c4385e5b`  
		Last Modified: Tue, 23 Jul 2024 11:10:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7778b778589c3c24a8e99893b405b8d9b63a14cb9b895d1bcb8368361081db3`  
		Last Modified: Tue, 23 Jul 2024 11:10:10 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1affc105a8d65b8ff888145f2b8960a0c3c6a6371de0d38e53c9d6b534e27d8`  
		Last Modified: Tue, 23 Jul 2024 11:10:10 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8d5b8a46b495471b0b360e5c0ce0f1df880ea31d62726248ecf0aff5f5c143`  
		Last Modified: Tue, 23 Jul 2024 11:10:12 GMT  
		Size: 19.2 MB (19209728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b0af160ec79aaa25d377994822803e83c7d3d242d1a80ecae3717586d3fae7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad8af13cf739ef256c47d004a56bea042b3316799707b27ff0cc1337545334`

```dockerfile
```

-	Layers:
	-	`sha256:b986b65b04ef91c367fa715ddc99e5eda463825a45509d71b070aac5fbec1774`  
		Last Modified: Tue, 23 Jul 2024 11:10:11 GMT  
		Size: 7.0 MB (7015530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:847a4b745a262437dfc483e5a78dc2ad5cf007a159bca7a8da1b2124d0bdda25`  
		Last Modified: Tue, 23 Jul 2024 11:10:10 GMT  
		Size: 36.5 KB (36458 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d38358b81fee2b9d7609ba0767ced8b4011fd1aa5cc0bf5b9b10d6ecfcf49426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157445263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510ba95a533c00963fc14071d6ee87c7d312068d71bd625eeaa937b9248f08de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c94b054af3824ad0d1125e76a629f6786b7bfc3ad1d0e93af25d62e248f51`  
		Last Modified: Tue, 23 Jul 2024 08:34:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d0ecf8b361c4d66e3bc3dff53f4f9f62d32b065a5fdc68175481bb4a87661`  
		Last Modified: Tue, 23 Jul 2024 08:35:15 GMT  
		Size: 69.3 MB (69326095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b6ad425e76f14bb4592a99e66018b412e5c5b24b446dc98070c425d0d8565`  
		Last Modified: Tue, 23 Jul 2024 08:34:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908e3b167b9ffe31302b987e30a82d20f5b70588426667528d88bf45f58d60a`  
		Last Modified: Tue, 23 Jul 2024 08:35:33 GMT  
		Size: 18.0 MB (18031915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958a057478b04a108e48b37c84347735bd191a74cbd30ac6540c79ceaaff28a1`  
		Last Modified: Tue, 23 Jul 2024 08:35:29 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d283e85ea5b5c829938ac886e448844d5712108536e4f9769950a40a4d58c4`  
		Last Modified: Tue, 23 Jul 2024 08:35:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d38196bd52a02134d917b282dcd51d87d0e2697379b1c1f57b9e080d0c2a7ea`  
		Last Modified: Thu, 01 Aug 2024 22:46:48 GMT  
		Size: 12.4 MB (12439770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c494ba1ef796f9dfbf0dca4f1209ab5fb1b1218f2a9055b52f4b720122cf0a9`  
		Last Modified: Thu, 01 Aug 2024 22:46:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b219f942d69b5afd754320da90118944f0fd9756f3916b5a69660b11d8208`  
		Last Modified: Thu, 01 Aug 2024 22:46:48 GMT  
		Size: 9.8 MB (9805351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d94ce04505ed2503dd98e1db37fb26a0f75ff90649873647a96fffc4f3ab82`  
		Last Modified: Thu, 01 Aug 2024 22:46:44 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b3081cf226b7ceb12b264d67af050fd0f20189f54d113dd0b3e6b7fcd506b`  
		Last Modified: Thu, 01 Aug 2024 22:46:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925784ebc5618064244687b44cf1a785c03b7912963f476c0007becf052bf5a`  
		Last Modified: Thu, 01 Aug 2024 22:46:44 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c016bda0a74cb971cce36d028ebb78232e328f12824dcea5162362bd25c00e`  
		Last Modified: Fri, 02 Aug 2024 00:52:34 GMT  
		Size: 1.3 MB (1309489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f959ddae84e2c0e4ffe7ec66e44085dc19f725d7842b1c6d51a379e8e309082`  
		Last Modified: Fri, 02 Aug 2024 00:52:34 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ee688b2fda56189564afd8ad4776353fe1e5792967ef28b81ff091a3b24b2`  
		Last Modified: Fri, 02 Aug 2024 02:49:54 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518ab1c0ef8f670e2b26590dda8d6836021008ecbe989d204fad295b34e9e40`  
		Last Modified: Fri, 02 Aug 2024 02:49:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb994ab49d7c8de80ef833e10ec0ed006445d95f3dd08b6d84b42b58c307cfb`  
		Last Modified: Fri, 02 Aug 2024 02:49:55 GMT  
		Size: 19.2 MB (19211268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b9a1f304462bacc47b0e99e1823149d90e0430cf928f5841103a72709a6128d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6861275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050c6b4d6851d53bb72a0e92d15155c11355ced9876d22879e26de887758fc88`

```dockerfile
```

-	Layers:
	-	`sha256:c76ec3d5afa81c4e7acc6ddffc2de8b8a655ad8046bcc2b438b97887a7938e28`  
		Last Modified: Fri, 02 Aug 2024 02:49:54 GMT  
		Size: 6.8 MB (6824636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f01b3014966893ea917848e35fbf3c29256aebd33bcfb722ee1c4028bfba24`  
		Last Modified: Fri, 02 Aug 2024 02:49:54 GMT  
		Size: 36.6 KB (36639 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:160800b92605ba11f97252e0c3964d8a49eaa03307ad88649e13b3f8b9b1e955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182217080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecca3a27e877e4457cf5360f4dc7f8895a19203698ec83977bb1da33e3500ce2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.22
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ea1dc36cca3c8065f64bcab06c8190d7ea87c67754f4dfa5f58787cf63576`  
		Last Modified: Tue, 23 Jul 2024 07:49:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b75061a10b60a63f9f01c424f5575d03426ba4335da9eb78c8fc778b1f20c0`  
		Last Modified: Tue, 23 Jul 2024 07:49:24 GMT  
		Size: 86.9 MB (86938666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53fca7938ec0579947ca273f587c83680d1e896c167aae176ac1100b0f40308`  
		Last Modified: Tue, 23 Jul 2024 07:49:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7074ac49d1e5d4e6a477167f66ac4fb6146d346e0e08fe86dc0ba23b9d5a0a33`  
		Last Modified: Tue, 23 Jul 2024 07:49:39 GMT  
		Size: 19.2 MB (19195744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d65af7135fabbe7fb3c59ebb32dde49c142be1829e226e5f76f4180f32a284`  
		Last Modified: Tue, 23 Jul 2024 07:49:36 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9248d4a69f9c97095ed50e8cbe85f22fe190231fd482d0d92394ce4ea5619`  
		Last Modified: Tue, 23 Jul 2024 07:49:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b974e22e0877e6aa5dd2aca5d30bfd20b553bcbbc7a2c814c001523951caeed5`  
		Last Modified: Thu, 01 Aug 2024 22:47:07 GMT  
		Size: 12.4 MB (12440532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e901ba69d01faa18ea063af0efa10ce9bd3fc335582ab78c7d61c1ba582b1f`  
		Last Modified: Thu, 01 Aug 2024 22:47:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cd1e28020a6a92ae89b7026de3834faa14b5b7857faf12f0bbc11514722ccf`  
		Last Modified: Thu, 01 Aug 2024 22:47:05 GMT  
		Size: 11.4 MB (11427800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f12aba60fa7ac8885e6680fa84c7b5c4842b09d89851219fb85873ba1dd6c4b`  
		Last Modified: Thu, 01 Aug 2024 22:47:04 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba166d1cbd39a006de397b1441b317a55fbb1637c157fa8d03ec8d751344c1c`  
		Last Modified: Thu, 01 Aug 2024 22:47:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0ba73b639e97bc9e8628e506e391e39ec2e3513467fb48bc6b796e0cce2c6`  
		Last Modified: Thu, 01 Aug 2024 22:47:04 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403649cde1508afc45b723430cfd40b86401f58cabd596b45137dcb99406363f`  
		Last Modified: Fri, 02 Aug 2024 03:38:46 GMT  
		Size: 2.2 MB (2194780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a4a04490d53ff15c276d3e7a82d0eb8d7d85c9c0a2192daca93f72fffd290`  
		Last Modified: Fri, 02 Aug 2024 03:38:46 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3958ce5a6480c79479bb92b4f9841197abd53bd931f4d3e1ac86d7f352a1099a`  
		Last Modified: Fri, 02 Aug 2024 05:20:53 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb4592ca5c67c7404572323ab6c719f1af9332aea67a2eeddf99790fcfbf28a`  
		Last Modified: Fri, 02 Aug 2024 05:20:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb767deae37a58bbfe94e17f376547737becbfe4960a26b7dbefebc746cde553`  
		Last Modified: Fri, 02 Aug 2024 05:20:54 GMT  
		Size: 19.2 MB (19211242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:203e066123ee9210801a643a7f892e091b915f346038d7c6cf6fe6e6c4aa2c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcb50c4de2ac56700c81d35e3b5847b76ff0f6384dac2704b29b3a533f84410`

```dockerfile
```

-	Layers:
	-	`sha256:28b39306756b25b7006b3a7d9ec3505537b6ee4b85c09a6011e6c30ab70fbf94`  
		Last Modified: Fri, 02 Aug 2024 05:20:53 GMT  
		Size: 7.0 MB (7018460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcee45ea261ce9f62ec60928a250b8745bf9a4c9ed67107edc32e0311a894ba5`  
		Last Modified: Fri, 02 Aug 2024 05:20:53 GMT  
		Size: 37.2 KB (37171 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:9eda252ce45fd0fd260237213c06e952fa45a9ea73d25382906ecf09ed56c96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190873143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b70dc6988d0afb1dc97958d6c21404b8b275470ab13515f1c9f1310604425`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af763934012d9ceff96bc82dc1e1c4cebed40efeec45843850c96aedc50f21d`  
		Last Modified: Tue, 23 Jul 2024 09:43:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff46c1a7152d5b4f388feb2531ce2f16a17c613bc5bcffd571983ad846d07cc`  
		Last Modified: Tue, 23 Jul 2024 09:43:28 GMT  
		Size: 92.7 MB (92720869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c931101488fce7030e5d9f32e6b097ef96703968a1f46e5b1846cae57f163ab9`  
		Last Modified: Tue, 23 Jul 2024 09:43:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16793e0add985a546e3e0047cb070a24e159f3e6cc286e0e2d54aa28d9bba4ca`  
		Last Modified: Tue, 23 Jul 2024 09:43:46 GMT  
		Size: 19.8 MB (19767347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910f43bfa8ba539b821a1c3785f2fd1071c8dea6560d9f79c9681a346d74b73e`  
		Last Modified: Tue, 23 Jul 2024 09:43:41 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1562793cf13f2cc098b633b1bba6e72bd2597c9ba9d050abc5d2f6025865b6`  
		Last Modified: Tue, 23 Jul 2024 09:43:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f18baaa11369f6d997a7b0c07813ed6bf61fc1c65da318d3b17a668acc9b213`  
		Last Modified: Tue, 23 Jul 2024 09:54:34 GMT  
		Size: 12.4 MB (12446481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4bbb9592f6a60a000bf96266bb6c0831a364a10c3aa4896047268a8edd74f4`  
		Last Modified: Tue, 23 Jul 2024 09:54:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578e70772939394b1ee0e6c6b8376d555e6c9635aaf66dfdb70c7b610f11b0ac`  
		Last Modified: Tue, 23 Jul 2024 09:54:34 GMT  
		Size: 11.6 MB (11586239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186e87a7f4698bae0dca7cc2a6512b0b6c46d045eb43e4813e7bdd86f21be7f`  
		Last Modified: Tue, 23 Jul 2024 09:54:30 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da5ac9abbd6c8f7e7a8708cf0179f8b3b7fcf631ca735eabc686ac9727812ae`  
		Last Modified: Tue, 23 Jul 2024 09:54:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1772d1e627f2a6fd05bd3c674dfdaf2ed4448d12c2a3e8e030eb1e2c2ea8cc`  
		Last Modified: Tue, 23 Jul 2024 09:54:30 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81713770a0c04ee2535d4e4a2f830042dfc861d784b1c30cd1cad3078b742cfc`  
		Last Modified: Tue, 23 Jul 2024 11:10:42 GMT  
		Size: 2.0 MB (1996247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69353f45e1fa08007887e1ea7db469241c77bf8771a5d9c11976448465730725`  
		Last Modified: Tue, 23 Jul 2024 11:10:41 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65349199380202b1f61d02279fa8ed3357b546dc935490a4e29676d097ad1183`  
		Last Modified: Tue, 23 Jul 2024 11:10:42 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faa501d33f955111d60398f3494dbb3bf3ef8507ca65551af308570a241b787`  
		Last Modified: Tue, 23 Jul 2024 11:10:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c45a059007454f3463bef4998667c219bc72d12662ff864a6cbf8a823ac489e`  
		Last Modified: Tue, 23 Jul 2024 11:10:43 GMT  
		Size: 19.2 MB (19209930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b94b90af41f28f45bdda76f2355613ce8eb9601e98239d194d01edc61f46eda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b2c075c6200e4e1439bd14be6202174ff0020dea9006955a5533098396b728`

```dockerfile
```

-	Layers:
	-	`sha256:e9af46bbc716a89e2f159983ac7d16e0e51c5896152a1e1c6cc31caed654723b`  
		Last Modified: Tue, 23 Jul 2024 11:10:41 GMT  
		Size: 7.0 MB (7006336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4752b3ae0799e7ac21efe7166a44ab866997d4969fc5d03ecfb8dae18f74854f`  
		Last Modified: Tue, 23 Jul 2024 11:10:41 GMT  
		Size: 36.4 KB (36409 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:b899c91a5391c5b7da5b547268c1c581d12d9ccd2c4d61cb7b22d37b0c5d2418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188439037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f97c641f6616dfc573339a8125cd1df952e28d64e64e901dac949eb899b67d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca31eac2ed8ece3ba386852bb9e717d3bcf925dea98a3ff93f0e61a8c1f9d4c`  
		Last Modified: Tue, 23 Jul 2024 05:19:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc37531317a045ead4f6cebdea9df0e36db3670bedacaf80e8221773f2aa98`  
		Last Modified: Tue, 23 Jul 2024 05:19:42 GMT  
		Size: 86.7 MB (86651319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4ba1d01ce6e77c2c36622a8a2a67c34e598bfd2f7d0447753e9ac4b7e9f051`  
		Last Modified: Tue, 23 Jul 2024 05:19:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa75568d7b5a74108a355894232865e34768417281a31ff6cff73e151c62b20d`  
		Last Modified: Tue, 23 Jul 2024 05:19:58 GMT  
		Size: 20.5 MB (20497178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb180c31525c409c0cfd8e90fbe903e0d136aab13077dedf5053a13b0fcb173`  
		Last Modified: Tue, 23 Jul 2024 05:19:55 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b1776164c8ab766bc2d7c4f16a9858876ae28e59b9a803e533f88e5bd8bdaf`  
		Last Modified: Tue, 23 Jul 2024 05:19:55 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7081d99a34f98bdaf4e432efd19412db16d04019d2165cb6ca33a7337c33b9`  
		Last Modified: Tue, 23 Jul 2024 05:29:50 GMT  
		Size: 12.4 MB (12447050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4edf013ee73b21ff38db1801527743251b6da15923b48000bafe4e68234f57`  
		Last Modified: Tue, 23 Jul 2024 05:29:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff704c87db150c76ebef57bed9fe871c9c740c71923a2095458196154168cb`  
		Last Modified: Tue, 23 Jul 2024 05:29:49 GMT  
		Size: 11.8 MB (11800984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df686871e4207bd27615f765a8f54a6c42d0c68d9c7574db649ae9cd9fb8a57d`  
		Last Modified: Tue, 23 Jul 2024 05:29:47 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27df4b23f4383708920066bec67ceee6c1c87187dde0917cd386b905be10067`  
		Last Modified: Tue, 23 Jul 2024 05:29:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192a6892878f79f9daaf1528afea6f0d99b8d02f2536384d0edd2276c8fbe43c`  
		Last Modified: Tue, 23 Jul 2024 05:29:47 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5421fbea6a552619e8fb0ccc8316555f308a5cb742ee8b8deca7c923d30c2348`  
		Last Modified: Wed, 24 Jul 2024 12:57:40 GMT  
		Size: 1.8 MB (1794342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955b3dbdd4eae4de5ef24247ffe82e6df83643a4221a2ed04a788f8f5bfef66a`  
		Last Modified: Wed, 24 Jul 2024 12:57:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2b386c5674567ccef16782072cc93e2084bb64cc7fac64ab6962a0a1a3ae4`  
		Last Modified: Wed, 24 Jul 2024 12:57:40 GMT  
		Size: 726.3 KB (726342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e806887e5df32bbbeb3b39372538f37fae419e2e9c323f3516a4339b6b3e8d80`  
		Last Modified: Wed, 24 Jul 2024 12:57:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d76b361fc1df08da1560c851597c819d8e5b3ae4605a8e11932466cf4b4fe8`  
		Last Modified: Wed, 24 Jul 2024 12:57:41 GMT  
		Size: 19.2 MB (19210729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:d50fc63966d182249e9b60d265437429c7342bc9ce5f6df5704fb06afe48a1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266f93a37c52961bf834299617d032a726313cb17112dd48489b4c8ec0389ef9`

```dockerfile
```

-	Layers:
	-	`sha256:404216893a5481ce325ab57321e0edcec726ba0e1cf2a136f50106931bc1d681`  
		Last Modified: Wed, 24 Jul 2024 12:57:40 GMT  
		Size: 7.0 MB (6981481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18088c8f0f4b757ed4da5d3ed1073277de8b73f824a20e4f4985142c94b1ce9d`  
		Last Modified: Wed, 24 Jul 2024 12:57:39 GMT  
		Size: 36.6 KB (36577 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:a90a74a9ee5a88b3a872d01c9eb8dfde759dc319cd97aa424b3564b07ae5285a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164977509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3ca63127a58a7edde2fae30400638ca6823df31a2a22972d977003028b9e2f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jul 2024 03:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Jul 2024 03:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.2.21
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 80
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22411513c35b4d7e3982ebff737af5ba004bdc5d62984cd8c5b651160a59f7b3`  
		Last Modified: Tue, 23 Jul 2024 06:12:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4474f9a1587d965f5ae0942ea7a9dc137ca4173b9421c9982ea957672948cc09`  
		Last Modified: Tue, 23 Jul 2024 06:12:51 GMT  
		Size: 71.6 MB (71640364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bed7a7890b32e00151d6716afc32f0c5bb7adea7e6ecf7448cce9d8d7c502`  
		Last Modified: Tue, 23 Jul 2024 06:12:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7600688f80d4e4de38d7739cd8d7f0e10309f5855b9c6045bae750d0992e8833`  
		Last Modified: Tue, 23 Jul 2024 06:13:03 GMT  
		Size: 19.1 MB (19105154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a76d1a80503341213a9ce748eefd88eb36f11dd8e11e428c22d6777db2185`  
		Last Modified: Tue, 23 Jul 2024 06:13:00 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8112cd17110b585495689bc2488bf63df180d9f61488545399e1e98417ad3c52`  
		Last Modified: Tue, 23 Jul 2024 06:13:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1f781dd41853207fce7d82bfb3f42c7e1e723ee8c642b89adf44cf7ff37afc`  
		Last Modified: Tue, 23 Jul 2024 06:20:24 GMT  
		Size: 12.4 MB (12446095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8be2e72d30d87bf860a82e63bcabfd3a7f50edef95f3070bf9c2c7dc41b96f`  
		Last Modified: Tue, 23 Jul 2024 06:20:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143205884fb88bce2331b48b81876b035c9e545413c85d86922e2273da116dcd`  
		Last Modified: Tue, 23 Jul 2024 06:20:24 GMT  
		Size: 10.7 MB (10650869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adac5f42a0daedab5f3e41737d9b6ad1c0acceb852292e16ea2abb231bca9061`  
		Last Modified: Tue, 23 Jul 2024 06:20:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b611349177140ea82c193c9d5ae3e5c41af7a7c61d6929025e8535d1e2791a0`  
		Last Modified: Tue, 23 Jul 2024 06:20:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f582aac1c7f61609ee0662679307e9aa9a0a247f7761957d96f1512a2261e32b`  
		Last Modified: Tue, 23 Jul 2024 06:20:22 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67771a1612bbe58d5e058544c107a692ec3d179a905503dd15bf2265d2e25ae7`  
		Last Modified: Wed, 24 Jul 2024 12:37:08 GMT  
		Size: 1.5 MB (1522582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da491a15b4a98fc7dd65c827dd18e24e7adf3608b361bc58d5341a849708982`  
		Last Modified: Wed, 24 Jul 2024 12:37:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2259a32d94ed077df651ee5e600bc4ca23dcd812c72b016640efd5e6ddc1a05`  
		Last Modified: Wed, 24 Jul 2024 12:37:08 GMT  
		Size: 726.3 KB (726348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d1974ed2e5b60f3054a575c23388db18a26d10dae620f7c1031b54896a3ee3`  
		Last Modified: Wed, 24 Jul 2024 12:37:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d2ea560a0a46f5be0866c442753a872029fcb6c67e650781e3d080027be5f`  
		Last Modified: Wed, 24 Jul 2024 12:37:09 GMT  
		Size: 19.2 MB (19211197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f0ba4bd69d00ba4564ce997be4f8d6e0c9243b356fdfac48d200bf7a04d72556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6882534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810cf3c64fc964470f8c3897e75e943677839df2d19af3a5711fed8d847429fe`

```dockerfile
```

-	Layers:
	-	`sha256:b4467e014b159af5845d0a3a0a175e63ac4caa179761958a181c5fe6a7deb185`  
		Last Modified: Wed, 24 Jul 2024 12:37:07 GMT  
		Size: 6.8 MB (6846022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f2fe3b42173cf420afced8ba0cfbca0c758c60aa876a2fd94fbff73e3d254c`  
		Last Modified: Wed, 24 Jul 2024 12:37:06 GMT  
		Size: 36.5 KB (36512 bytes)  
		MIME: application/vnd.in-toto+json
