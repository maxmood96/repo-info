## `drupal:7-php8.2`

```console
$ docker pull drupal@sha256:d49587b3491bb6c1ff97b51e628247966cbd9f283751059a97b6ec5a53e7aed5
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-php8.2` - linux; amd64

```console
$ docker pull drupal@sha256:944a33784a6f334b73610fc13136bf3c78a6a52eb5e08100dfbe315afe81b148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183018792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa4fd9d6e6711d4cc8fee7fe2c919f230032b54bac71a8c4296f7e9ad6b4db0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c386db9cb1d87e70bc4655a9f464379178e6faec37925b32f481121cd1fd6b5`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef1b237c949fbfc49af0024af5189a1feefff253e445a7b19ab4327ce5a5909`  
		Last Modified: Tue, 13 Feb 2024 07:33:11 GMT  
		Size: 104.4 MB (104355255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c66cb68b0ffb6ab95a1aa748b4012b5da8077a4a4c14a3f9bebcf9bf02f351`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c790c1c009dd7204cac7a35fd9151636c23f96ae965fec6263addd5d366c547`  
		Last Modified: Tue, 13 Feb 2024 07:33:38 GMT  
		Size: 20.3 MB (20303944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055748d0b38a426b2cef949d76f35fc04c5a9a9a66a2d40449219a4853635cf`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d72b3b895bccef06314fe3a5818d977b5b695a9e1a698eab278c1138790f8`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a354636f862b01c059c1bfb98b1fb5690dee04607860bfcde46df979b83e0745`  
		Last Modified: Tue, 13 Feb 2024 07:42:05 GMT  
		Size: 12.4 MB (12408680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139fa831a3e6a192d9c34b51da2278bbc21b59818211cad69aa0afae9cd1732`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17106305d52519fd77cf6375c68dc5af30746038c372d15c8afb53bcdcb4c68a`  
		Last Modified: Tue, 13 Feb 2024 07:42:04 GMT  
		Size: 11.4 MB (11404904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b86f20916c18b1fb9b329b32e4f8701ebdc9191b17f4be6bc52fa3f3215e50`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa13ba4f6f48ae2301250cca77c42706fb9e7566d701084f7f9d5a3e498c2123`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fe7754d476224d8cbaf01f8c02b87e12b08c9fbf6d6f19716d0e3b64e4e89`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52727dd399fea6f239d5714584a74390a7d6f1400df7e0dcf12f20ad644c8cdb`  
		Last Modified: Tue, 13 Feb 2024 08:57:41 GMT  
		Size: 2.0 MB (1997156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946ff408a86ca20254eacb0921984643c886ce8732c67b3c2656df89a84a97e0`  
		Last Modified: Tue, 13 Feb 2024 08:57:42 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc657e738fc9252cc545c0cd366545623b117eeabf0fd784c8db4402b3bdb992`  
		Last Modified: Tue, 13 Feb 2024 08:57:42 GMT  
		Size: 3.4 MB (3418880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:1cf2df732209a583626d6a5c28ceda9450230b248446ff3d6d0b301eef944b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d436fded7df6b4c4f91d33758322204943dfdfbb9cbe2394e68b387e946202`

```dockerfile
```

-	Layers:
	-	`sha256:2917a4de89bb1618880cea52cf903b66d9cec83fc7a37fb2d71659a8888a61a0`  
		Last Modified: Tue, 13 Feb 2024 08:57:41 GMT  
		Size: 5.9 MB (5864350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4736d8ea0cde3878cad468f1331f8c885a210777cbae54a5f9f676a8fd0637`  
		Last Modified: Tue, 13 Feb 2024 08:57:40 GMT  
		Size: 28.1 KB (28054 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; arm variant v5

```console
$ docker pull drupal@sha256:e512093322224fa0992a4a5a660fa252982a31664e4fbd1887bcd422b5130ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156215946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c99cd945fad287b1beb340152a0b372a7402e6e31b2c4bb1bd1b7fcf92688f5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8283139cc6d4789aed1133c6fde1612dde4ad0e619393c6954814a4b4090ae`  
		Last Modified: Thu, 01 Feb 2024 05:35:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a3536e12257687ba92f6da225527039c7338448f32f80a997251c5e361625`  
		Last Modified: Thu, 01 Feb 2024 05:36:04 GMT  
		Size: 82.0 MB (82002660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a9d60527acc46dca56eacf6f29f5808db96b8f03bdc8736a526c30c2b434cc`  
		Last Modified: Thu, 01 Feb 2024 05:35:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb940fd811c9b5f293f68c29cfc438a728164590cc05c3db84c4e6dcec9f73`  
		Last Modified: Thu, 01 Feb 2024 05:36:55 GMT  
		Size: 19.6 MB (19609431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7a66c6cba78886e236c9efceed714c445f675b9657dbf03da0c5ddbc839b0`  
		Last Modified: Thu, 01 Feb 2024 05:36:52 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5659e1db3f935550e44b4831b120d31ca577e432ea967ff248d37efe574161e3`  
		Last Modified: Thu, 01 Feb 2024 05:36:52 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f67fdbfbe71acf4417ed9434a942eef329d911b4157daf3e729788e1633e688`  
		Last Modified: Thu, 01 Feb 2024 05:40:22 GMT  
		Size: 12.4 MB (12407876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653b86f3b2d9dea82066f5f29592b301fd50bb6eb1646b535adf3b81bef77b2b`  
		Last Modified: Thu, 01 Feb 2024 05:40:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb34db0062b09b096468d3f7e21bb2de6dea4916640b09e9535ec45f037c10`  
		Last Modified: Thu, 01 Feb 2024 05:40:21 GMT  
		Size: 10.4 MB (10389358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff6d282950bbd3cd4f375c0338ef54b081348959f99281f50b7b150de1a702`  
		Last Modified: Thu, 01 Feb 2024 05:40:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da500cdb81377f75b2f225e647cca8de537257eb98566ed0731c502fcbb7640`  
		Last Modified: Thu, 01 Feb 2024 05:40:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf8cb6c8e48220637b744130a1272d379fcff5cabbdc641fe638df1d515c064`  
		Last Modified: Thu, 01 Feb 2024 05:40:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4fb317f64c4877b8ddc90df8e994f70bc51cbc3363726b563a80611d929170`  
		Last Modified: Thu, 01 Feb 2024 18:55:43 GMT  
		Size: 1.5 MB (1472533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca5084444edb3bbc7b75b6bb392de029489fc8af79456c1c79e6a9b310c21c0`  
		Last Modified: Thu, 01 Feb 2024 18:55:43 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ccb17be8102ff80648a0cbe662175975aed3cff2a47530d397a2a4581242da`  
		Last Modified: Thu, 01 Feb 2024 18:55:43 GMT  
		Size: 3.4 MB (3418875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:c9022aab802b95201837dd69f074541ff7b07089dbaac5f64c36ada9e2000358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5728088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f248b3099265948a0b59d878009a88dd4ab50d0ae777ed0b2be129703f7e4f1`

```dockerfile
```

-	Layers:
	-	`sha256:fe0cbd33b1fbdd20c90c78c5785ddaca570cee5fbd5f853c7f0e74fb8d4c40c6`  
		Last Modified: Thu, 01 Feb 2024 18:55:39 GMT  
		Size: 5.7 MB (5699927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3a2bf7bdb58270ff7669488c2f167e8c4385b791eb3027dba1cfdfcf78abfe`  
		Last Modified: Thu, 01 Feb 2024 18:55:39 GMT  
		Size: 28.2 KB (28161 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; arm variant v7

```console
$ docker pull drupal@sha256:c5176cf1bfc0b639d401e3741fc8eaa9a79f87b34e22a3441a8692428c2fd6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146964260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1d7a3affc0ac799de4fece97fa3d8ba3be519edf88853c4d1b2d9db316cd5d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391138267e710c3afd1b13ba20349432d550fbb6ca24d5c03c761feae22b88ee`  
		Last Modified: Thu, 01 Feb 2024 04:24:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc30a445c6e4bf057f6d7fb3a4548be66cef938aca0884681b2602cf7807923`  
		Last Modified: Thu, 01 Feb 2024 04:25:04 GMT  
		Size: 76.2 MB (76169686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2abab10a7e661e57eca65741d4ee689ebb206370db90b4c05c93aa3b7afce10`  
		Last Modified: Thu, 01 Feb 2024 04:24:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c27433b27de38bd46689c5ab4ea8a423bc343feebaea73d1d20d2aa314da3e`  
		Last Modified: Thu, 01 Feb 2024 04:25:49 GMT  
		Size: 19.0 MB (19046603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1fd23f93df4e6bcc7adb049f7e12804c6313798f3ceec63da7db141eed10a8`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649568d520a69772a79a3e5c4ce6031b6f2f7e274993c07bb783e481941066ff`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe2c127a46474022cc69e7ab8271858708631787a77ab94ffaa600e5eb352f2`  
		Last Modified: Thu, 01 Feb 2024 04:29:27 GMT  
		Size: 12.4 MB (12407860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1daa5547ed933b4460fa4dfe771b898e2f3e75ce7f99cb3a200a8c54748266e`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463e5207c526ebce9c5b4cf701e473e1199d310fbeb4787cd93619db99743a0`  
		Last Modified: Thu, 01 Feb 2024 04:29:27 GMT  
		Size: 9.8 MB (9819710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289557b5f69d251afef4200ff3e54c5f77a41457acd92715e7c9c1b0b0312de2`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60bbf7f7b83cf61f052a2eca634b228db210099d4ed918b0bac7e6db940fe27`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeee08a95fa2936e7413f4697356510c2b22ad55b9a16f5f769be6124a50f3f`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be284d71b4c5ad9c1a7d5992ae599c79aafb706796588bb378a01cdf1c5d5ad`  
		Last Modified: Fri, 02 Feb 2024 15:34:10 GMT  
		Size: 1.4 MB (1354080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caedbf490ef9c9f3ce0921b07ed39041fdb63e33718e840500c3aa7e3f68ff1a`  
		Last Modified: Fri, 02 Feb 2024 15:34:10 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962d90a47bf0f1569e669194624a5c9047ca224fbf1bc90fe761dfae7a11e951`  
		Last Modified: Fri, 02 Feb 2024 16:42:28 GMT  
		Size: 3.4 MB (3418881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:2739cb5856e4e1babd8ceca8d676a767273b1bdd8e6da364bc63b12997ef39d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5729962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7207b978872c8ae62d7b428237bc92aa7b02cc9a84300a90dc78627a025f739`

```dockerfile
```

-	Layers:
	-	`sha256:4d35226209f02289b33c6f2d228d84756a990cf21fc3da0d0354dbbe229c86b6`  
		Last Modified: Fri, 02 Feb 2024 16:42:27 GMT  
		Size: 5.7 MB (5703913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a81cd2aaee8e0d75458b7259b48c49c19981ace73a62ea0fed7c9e8bebc0b6`  
		Last Modified: Fri, 02 Feb 2024 16:42:27 GMT  
		Size: 26.0 KB (26049 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ec3218ba6d8245cd2f4b1117dbc9a1c44ec2361886ba3cdfdbd362eec3d148a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177086888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c8f9c76960716a301804d6cdba6281c29fe4eb8d122a095498053ac86c2c57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7a340515b48e1c129ae5f32a9749bddee1f8e8329b7598fcbf4d08bbd6fb1`  
		Last Modified: Tue, 13 Feb 2024 07:00:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290f914abd180febe4ca21f26e7dbd62a7d47b3e0c2bb607b502ef0420c26a39`  
		Last Modified: Tue, 13 Feb 2024 07:00:29 GMT  
		Size: 98.1 MB (98125913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa77fec9d8935ca4f47917fa1800499aeb09f491467b65b0914b9598f905ab`  
		Last Modified: Tue, 13 Feb 2024 07:00:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e32a81172311d82a21a8c59c44a19943264d56868424bc14043cf6100b2fd`  
		Last Modified: Tue, 13 Feb 2024 07:00:54 GMT  
		Size: 20.3 MB (20305132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4064de42914748cf75888bc76bce8469dc92ae858893c597ede2741b140c622`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1ed550d4635090d82d30c08e1d408806bfba8c24fffe9004f3b0837df191b`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29386a07b0fb38b6f26a5a8c069cad0296b4554cee7ca6d835d589aba41462c`  
		Last Modified: Tue, 13 Feb 2024 07:09:04 GMT  
		Size: 12.4 MB (12408227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a0d2ccf9bb28e54c8b6e5ad86add1a87bfb22761da9eb7ea8bdf4b7ebdd8e`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec30c4cb990f53b935a7f8bd9190a5c37fb2d7c7427b6c7b14e3e1ec73ba2a56`  
		Last Modified: Tue, 13 Feb 2024 07:09:02 GMT  
		Size: 11.4 MB (11411295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da02d12faeeddd5da284c9bf92ff195f1105bef826ab21ba909db967793c03c8`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de9da0d9fb698f29b8b078b7b96bc86b5456666d456c2606fa10d22b4b8d94a`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe3329f8e7716983d4634d2eb72f9a31acf2b043ffec645c05faad08bb47cab`  
		Last Modified: Tue, 13 Feb 2024 07:09:01 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e420d1beb619d5d9fe069037e74c55da92474e117b20c160b98222cea6f759`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 2.3 MB (2255203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb1c87f379efa899c82110076efc2b8d35840fe6c5380e070d72809de33692`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a682ac5f14c5319cedc24ebc5aecc1ca10b44cdd49fad6f06c473388ce30c5aa`  
		Last Modified: Tue, 13 Feb 2024 16:39:34 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:71c5cea9157c6ee076129de842b06a231fe52844fe0bbd8500b66cef8ae3079d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6e95ccc6dfffbea1b037406e5d624bdac62f9e8e41a744249645d3406ecb3c`

```dockerfile
```

-	Layers:
	-	`sha256:e40d484d4f44d76097d865974dc5f248b0d8ab15a2551a4504f4a372f0d5f451`  
		Last Modified: Tue, 13 Feb 2024 16:39:33 GMT  
		Size: 5.9 MB (5889361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f471ed00cf8559b9c7e198304ececd4911c84a01bfefb4bb0012c029f42ee94`  
		Last Modified: Tue, 13 Feb 2024 16:39:33 GMT  
		Size: 26.0 KB (25955 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; 386

```console
$ docker pull drupal@sha256:09d245ae0ea3e0d9e1f881fb70c8e2a0b2c27ce7663d46507fd50db66785a194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182008731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfbcbb516f153a36403b90a9c5bdf94420eae16d2703be2f35aeeb29c55a094`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfde49385a90835b9c1612c002c49650aa228e709c6bec76329576d154acf40`  
		Last Modified: Tue, 13 Feb 2024 09:08:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ed10d21879c841ec1dc9f3c51bfc996313547be9838dd0871e0c090e9db93`  
		Last Modified: Tue, 13 Feb 2024 09:09:19 GMT  
		Size: 101.5 MB (101519769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0108a981d683eb4695cf1efac3357088358d8bd27fafb095510dcdc689e9270f`  
		Last Modified: Tue, 13 Feb 2024 09:08:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa94a6b92707cb45a0ff3ab809cb18c5a53cfcaad6fb553c591ef3b376088a1e`  
		Last Modified: Tue, 13 Feb 2024 09:09:47 GMT  
		Size: 20.8 MB (20826088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ba0ea043787178dd74139db437ce2498a8d3bf85e4eed296ea8e55a598f5a`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ec064cfc067a6de6b378be145b2249b472d81b6fbf511d5f614fdf9909cad5`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f319fd9049ee21eccbb2c23231019d3746d7634ea0bfd69993f02efcf8997c`  
		Last Modified: Tue, 13 Feb 2024 09:19:17 GMT  
		Size: 12.4 MB (12407595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58504e4335c41bed822efa4ad7b25f791c5cc6d9083b99d25943fed18891bf68`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19276e3afb9f25daf34037f4d19ea0302b5350ded9a2d2a89bde7ad1c08bd7b7`  
		Last Modified: Tue, 13 Feb 2024 09:19:18 GMT  
		Size: 11.6 MB (11638109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f11b92ecacf55e1b3d78edbf5baccea90e44bbc062a77468ce5f01aae4ce53d`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de8b000ea1dc85d6489a771eacacc0b89a42714ac3564896f2a0f87ec18647`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec0f7e99cf4670b71f0f0410acde2e2986034b5cca05650e313a5afebcfdf52`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f9e95a40ad706d2479606ed585ddaec0be194ea468cd6f9a60cc122c1bf8f3`  
		Last Modified: Tue, 13 Feb 2024 09:58:12 GMT  
		Size: 2.1 MB (2050605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877eb105d2d5b5dce22f59db6c057ba76803bcd53029a1b299b0c841f5b9dc77`  
		Last Modified: Tue, 13 Feb 2024 09:58:12 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9ce8815f1d6d5716f7bbff800c59cdc01b871087e36faa3a36ffd1e6b33a2c`  
		Last Modified: Tue, 13 Feb 2024 09:58:12 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:7829901e82f4f205ac1e1b85c2a5ac6032bfdee6c1eeebc3a754871f687256a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5874486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3074d62000a6fef419dc5f5b874dd2ec8654b17bd76ef99f7537b4021da767b`

```dockerfile
```

-	Layers:
	-	`sha256:92ba7a0fc64382ce25949508a9561dd7ece86a6a937dc6c56c60d3054f598466`  
		Last Modified: Tue, 13 Feb 2024 09:58:10 GMT  
		Size: 5.8 MB (5846476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7ba376fc24207c9055d570e33f08a816f27635c05d1b7a7c00820d596609fe`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 28.0 KB (28010 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; mips64le

```console
$ docker pull drupal@sha256:86d20b2d58169bf3a4001964e5c5301575f2da415f1435032b7e9661b08d99a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157355512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8582a856228bc6718e220f130f03acd151d548f756314863460403cc1a2f0151`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ebb65e9609a134ca261110d91316da52ba4c8a03bfd1b6042eeb118ecdc0d`  
		Last Modified: Thu, 01 Feb 2024 05:32:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77b8b149903d54558fc3eec266d39cf2b61f58f5203ccc26d58112b8e6d7b6`  
		Last Modified: Thu, 01 Feb 2024 05:33:45 GMT  
		Size: 80.5 MB (80476508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16027d9f3960d20f5345a8ec7d3d2b4aac29edd4dbe7bbc7c59edae2477c225`  
		Last Modified: Thu, 01 Feb 2024 05:32:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08875822110c5006e651f11f314cdef61c176a7ab201e33eacc231bc150a5f38`  
		Last Modified: Thu, 01 Feb 2024 05:34:46 GMT  
		Size: 20.1 MB (20053868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da8381986736893413722065003cdacb7a3fccd4dd66d807a46ed86d80df36f`  
		Last Modified: Thu, 01 Feb 2024 05:34:32 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050e85b706826b82301b4d2154016ead10645b801383a6ffef2fdc79e6674c2c`  
		Last Modified: Thu, 01 Feb 2024 05:34:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde9c0bfe568446be1d361ac908405ae071fa2a1ef69cdeb63f43a003d582ab`  
		Last Modified: Thu, 01 Feb 2024 05:40:36 GMT  
		Size: 12.2 MB (12201904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0031140140307b2b5c1d8dfd63f4a3337a65c900c31c897fe8859ba1ad956b02`  
		Last Modified: Thu, 01 Feb 2024 05:40:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfd7e3bf912895993565cbd34383c865bd9515c1b04691de0e20337164c8e87`  
		Last Modified: Thu, 01 Feb 2024 05:40:39 GMT  
		Size: 10.5 MB (10484972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874ada6a1b46a84454f2926d4418bef67162ea60e3ce8d826008e66f1a8c734`  
		Last Modified: Thu, 01 Feb 2024 05:40:31 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb77b59fb134c59af42fcd53c8b9faadffb19d931105d88e19e13d33d1db26c`  
		Last Modified: Thu, 01 Feb 2024 05:40:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fce977b9b7b98a00ee6c7683df565113e44ce9a9861d63ab164ae9148736f2`  
		Last Modified: Thu, 01 Feb 2024 05:40:31 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b7762c5f9f91c54098e6d20fc0fd73e4a30738454ec7861bdb2598f8b45540`  
		Last Modified: Thu, 01 Feb 2024 18:54:05 GMT  
		Size: 1.6 MB (1571151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddcfc3b49f4ebe7d21fc51fa3aad6321402669ed2de70eea7230f25ee138959`  
		Last Modified: Thu, 01 Feb 2024 18:54:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f04750c0cff10f54a97a55727590685659d2e2176ceb5167f85ce4982a03f`  
		Last Modified: Thu, 01 Feb 2024 18:54:06 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:24f8eb517bbc8011c2d1e0146ed2bad98aa38ea2ef8cf1735cf502d456f1df62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 KB (27915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d321301255d7d46e5008af473a7a62af2f59c39abef0bb9a10c31bd3af9bbceb`

```dockerfile
```

-	Layers:
	-	`sha256:c44002bf1377460ed840e9876afa5834f543c88228c24aa34326b30f10092877`  
		Last Modified: Thu, 01 Feb 2024 18:53:57 GMT  
		Size: 27.9 KB (27915 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; ppc64le

```console
$ docker pull drupal@sha256:eab9a4c9dffca773691636e30eeec73c2b7290acf7ead74df1ea252ea877ac12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187423685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a19e460c44a7ceb5a61f2aa39c5b4bd9f96fce0c53fc9e5ede705373339d47b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f1023e69b0297ca1b43f02b0de9f2700c16c9f3bc3cd4d532dce1fed98a82`  
		Last Modified: Tue, 13 Feb 2024 06:43:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c21152df6e3694f2bd61235e4c23ee7e24735cd91cfff9f6dca5abb307a801`  
		Last Modified: Tue, 13 Feb 2024 06:43:58 GMT  
		Size: 103.3 MB (103313095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0608cc469fd017def730be29629f988d7db21971cb60c627d4043f3f4ff24e3d`  
		Last Modified: Tue, 13 Feb 2024 06:43:40 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86cd418ad9f36395f647795ce8a6ee67f8cc57ee87b45a13e843c0d2209c3f`  
		Last Modified: Tue, 13 Feb 2024 06:44:28 GMT  
		Size: 21.5 MB (21489555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82afa6fa26cbb0b105f3ff50f1bb25a7743b2fb1e1e56092bf210cfd7a63d9ae`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20423759eec7201d4e061fab44ae4f2be21b3cf195ccf90ecac69aa7ff61e45`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42550739b7f48af716ac832fad1934c3cd65a3af5c7b62a26902f47601927316`  
		Last Modified: Tue, 13 Feb 2024 06:54:14 GMT  
		Size: 12.4 MB (12408126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46df924d7eef2bd9e70044d4446be91fcdefdf371aace2a0259973ccc336aca8`  
		Last Modified: Tue, 13 Feb 2024 06:54:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167aa1659e64fadc6152357b3e6abc6d28f56a25b8076d22275d7bd36a9e03cc`  
		Last Modified: Tue, 13 Feb 2024 06:54:13 GMT  
		Size: 11.8 MB (11813243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8043b9d3bd33a06672fd37521b2445df2f9f85b8b52d9cc56969e67c45fb2d`  
		Last Modified: Tue, 13 Feb 2024 06:54:11 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1dfca68d509a1142b3fb23a5a6367e0ae0cb5474e4830eb706f009e87c99c3`  
		Last Modified: Tue, 13 Feb 2024 06:54:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ecf1b755b47018e22491beb51c9f16a806520903e77beea5834e58b541781`  
		Last Modified: Tue, 13 Feb 2024 06:54:11 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b2152b82db0166f33f5e101583cd23e2d2396e09aa7800269ea85c58d0333`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 1.9 MB (1855994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81eb21cb90f51556902eb814ce835b9cb3add072d84e52ec75670028d50bc8`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cb8009d5720329168fe1188b52e68d3236720b84b288b06c23636284e9bfee`  
		Last Modified: Tue, 13 Feb 2024 14:53:44 GMT  
		Size: 3.4 MB (3418880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:f306625c027891900aedd99196d5a326765602ec2dcf9b06037493fb6f86cd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5871688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5613f1ba878c886b67d1d15461c16779e2c68596985b654574b4d2dba14644`

```dockerfile
```

-	Layers:
	-	`sha256:857df546142640b08b4897db3444f18c44dd140ee7df8282abdd3e667dc45060`  
		Last Modified: Tue, 13 Feb 2024 14:53:43 GMT  
		Size: 5.8 MB (5845689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7efd69cace4e9485bbac6f33500a99d97fa26f892cfa56e9924aa0c6e4b7bdb`  
		Last Modified: Tue, 13 Feb 2024 14:53:43 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2` - linux; s390x

```console
$ docker pull drupal@sha256:22b210e9016bb464ecd85f381c462fae699cf10552aec78e525390afbc58fb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156253738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c595634e4740dbf7ef68f5a405a697c54b819d0ba7dd5a51448216948499977`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 03 Jan 2024 18:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 03 Jan 2024 18:58:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.2.15
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 80
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["apache2-foreground"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba508c7dad7497a6bbe373c417feff78e2fa3227a96337a55b59fcff9da5ae`  
		Last Modified: Thu, 01 Feb 2024 03:18:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59819a0dd4fd287d9e24157644eb1ff924fbb16ef9cf4e30d72908e1308d18a`  
		Last Modified: Thu, 01 Feb 2024 03:18:33 GMT  
		Size: 80.8 MB (80818276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdcf5b86b0e0f5aa0697cec9b64981a167285c1a2724d924a086a18d2918f20`  
		Last Modified: Thu, 01 Feb 2024 03:18:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebd6cefe388bfe27d4a3bcf090a9de9f6c9aa33af40be2a2395ada6c5f097d`  
		Last Modified: Thu, 01 Feb 2024 03:18:58 GMT  
		Size: 20.1 MB (20084952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e4d9603325f9c8f157cc8090da6b4417fceb3c7a6a361860b8b52b4d64c9b`  
		Last Modified: Thu, 01 Feb 2024 03:18:56 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354950213319e1bb7f0f4e7adefdfafdf4e04ca12eb613e84acbaeadd3836a23`  
		Last Modified: Thu, 01 Feb 2024 03:18:56 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0102a161406a0521fca45d00343bd37d2d48b7194c66e781f50b683b261008`  
		Last Modified: Thu, 01 Feb 2024 03:21:40 GMT  
		Size: 12.4 MB (12408138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b8a30d53dae92b4ba19c3c334d8ff1ddf41cdc346a9ccd683060a546ebf7bd`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf3ba60882e47ed69aa7a680ac0026920e27ef8a56e54edce16c3a410bb1276`  
		Last Modified: Thu, 01 Feb 2024 03:21:39 GMT  
		Size: 10.5 MB (10450085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa51cd076b6bb332388f0c8ce8590fc455e1da472165a84176be54858a15ca1c`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e28100cd16736ce346da1727d5e46972524539e3119ad3b27c11e5115884582`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfb1c5076dcecc11fbc4c0174c55c7af4b87a17945cd2812db07815411518d2`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de55b4bdf8afd27ff594ad3c13a7aa1b7d8624e3ff62e299f4c4832190afa9`  
		Last Modified: Thu, 01 Feb 2024 21:28:30 GMT  
		Size: 1.6 MB (1554055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e739da822cb801185a20d0bae965c2e48b341870bf716473ddc186fd8af0e8`  
		Last Modified: Thu, 01 Feb 2024 21:28:30 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d21187ae2fff85789ff20345a966d95a4d4818afc4c3971e1ba43e0600cd3b1`  
		Last Modified: Fri, 02 Feb 2024 09:47:22 GMT  
		Size: 3.4 MB (3418877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:2dd0d027f2dd43ef941b8fa3a26fafcbe254d55bef7c9eada726026661f719e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb8e9f89f55e4b35bf70309fa57136e056baa3dde28dd6a016ed55797523f3e`

```dockerfile
```

-	Layers:
	-	`sha256:0899d1715a0d22fa3caf8ec7df23f9f763337373c712394dda4cbfc1b4924713`  
		Last Modified: Fri, 02 Feb 2024 09:47:22 GMT  
		Size: 5.7 MB (5725796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a169f14da31592605b0a6df2f3bcaa1fe0c255363232ecd0742384dad3f4a71d`  
		Last Modified: Fri, 02 Feb 2024 09:47:22 GMT  
		Size: 25.9 KB (25941 bytes)  
		MIME: application/vnd.in-toto+json
