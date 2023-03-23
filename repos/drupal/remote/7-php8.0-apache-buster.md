## `drupal:7-php8.0-apache-buster`

```console
$ docker pull drupal@sha256:934359209049eeaf085047d29b33a6e185f2ac7610a5e25bdff4e0120ff642d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:7-php8.0-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:b38ee41e2ca2563e1c2c71c68f0553f4aeffc389c89480c600fdd9d06bdf8bca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150042474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd06971c0fe017219824162b19b70f511f450931f7ebadd4412f6411b9e9eedf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 12:19:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 01 Mar 2023 12:19:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Mar 2023 12:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Mar 2023 12:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 01 Mar 2023 12:22:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Mar 2023 12:22:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Mar 2023 12:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 01 Mar 2023 12:23:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 01 Mar 2023 12:23:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 01 Mar 2023 12:23:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 12:23:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 12:23:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Mar 2023 13:15:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 01 Mar 2023 13:15:53 GMT
ENV PHP_VERSION=8.0.28
# Wed, 01 Mar 2023 13:15:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 01 Mar 2023 13:15:53 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 01 Mar 2023 13:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 01 Mar 2023 13:16:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 01 Mar 2023 13:19:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 01 Mar 2023 13:19:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 01 Mar 2023 13:19:03 GMT
RUN docker-php-ext-enable sodium
# Wed, 01 Mar 2023 13:19:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Mar 2023 13:19:03 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Mar 2023 13:19:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 01 Mar 2023 13:19:04 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 13:19:04 GMT
EXPOSE 80
# Wed, 01 Mar 2023 13:19:04 GMT
CMD ["apache2-foreground"]
# Thu, 02 Mar 2023 00:50:59 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 00:51:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 16 Mar 2023 00:31:32 GMT
ENV DRUPAL_VERSION=7.95
# Thu, 16 Mar 2023 00:31:32 GMT
ENV DRUPAL_MD5=ebd3b1ef8605585d703c13552f841731
# Thu, 16 Mar 2023 00:31:33 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83b3ecc128c09ea7b53df46a0fbf2971d9dc77ac2893e52bc2784760a829c35`  
		Last Modified: Wed, 01 Mar 2023 13:30:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f0a974ccb7229aa047aa19e0fdbd29ef937f0ab2611c3d9265c383ae81b77`  
		Last Modified: Wed, 01 Mar 2023 13:30:49 GMT  
		Size: 76.7 MB (76693078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b974206414d9913df844efe41244bb1274c99d9eed1d2e818619ef9347fbc90e`  
		Last Modified: Wed, 01 Mar 2023 13:30:38 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7311be4befaaecefd363f933e93243768b5ce21b0a1c789c8470ad8482f15f`  
		Last Modified: Wed, 01 Mar 2023 13:31:16 GMT  
		Size: 18.7 MB (18685426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3b2e237166fb1c37dad149e0f5a982f11e02e4ecc09680c81acdd98cb7f9af`  
		Last Modified: Wed, 01 Mar 2023 13:31:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023f8f4fcf29d6f222771168be5980e65a9a7928482bf7a3a82354fdd86b06a`  
		Last Modified: Wed, 01 Mar 2023 13:31:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ecf61979e92ada9860deae6597f8df95c08f51d167ce4a2961dc1cb6b82ac3`  
		Last Modified: Wed, 01 Mar 2023 13:36:18 GMT  
		Size: 11.1 MB (11141067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66236a7fe2b4fb59f8f675e7ffe5a03b9d3d9b7d9d290222f5e7260c255640f`  
		Last Modified: Wed, 01 Mar 2023 13:36:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84792bd7c7a03e127a95053ccc759efae1f2011fdc0709c3f5ef6874f272218`  
		Last Modified: Wed, 01 Mar 2023 13:36:17 GMT  
		Size: 10.7 MB (10726507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7960e776b6cc20bf66889ac9a68379f37d6aba322868375ce3cae4aaf6bc7e72`  
		Last Modified: Wed, 01 Mar 2023 13:36:15 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7a779e7b5398af0b495be79dad74edf57c4be58bf540a3cc99b71d7304335b`  
		Last Modified: Wed, 01 Mar 2023 13:36:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1820ec42b402e9bd6b1f51b16d09437db160f8b341974ee90ce7ffab9825830`  
		Last Modified: Wed, 01 Mar 2023 13:36:15 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee976e55d8d8cd93f6f2ec7e5d3cd9fbe435cbae34e4340966d8268a79723b76`  
		Last Modified: Thu, 02 Mar 2023 01:08:00 GMT  
		Size: 2.2 MB (2247855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ca503790f559df89a6b3909e9fa0bf08b280905f0371f1a0ab2e5d38721164`  
		Last Modified: Thu, 02 Mar 2023 01:08:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77585dd67e39673f9703f53f253a4e9f253b76a9506b193b7e26712d42548e69`  
		Last Modified: Thu, 16 Mar 2023 00:53:37 GMT  
		Size: 3.4 MB (3402775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:e8c8f2a270ed430df496fe92718bcbdc929f436040f7c37d3a21fd8a9ec0a5c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125211212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f772db8d05d6dd5a5d7922e73b3c42be3784ae44a77cf796d0cf71bded6eb31`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:33 GMT
ADD file:b3a5424864097d73516302c7e0a8fe9394880555c85f25a82a020ec3fc887eb8 in / 
# Thu, 23 Mar 2023 01:20:34 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:02:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 10:02:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 10:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 10:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Mar 2023 10:04:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Mar 2023 10:04:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Mar 2023 10:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Mar 2023 10:05:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Mar 2023 10:05:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Mar 2023 10:42:23 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 23 Mar 2023 10:42:23 GMT
ENV PHP_VERSION=8.0.28
# Thu, 23 Mar 2023 10:42:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Thu, 23 Mar 2023 10:42:23 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Thu, 23 Mar 2023 10:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Mar 2023 10:42:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:44:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Mar 2023 10:44:37 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:44:37 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Mar 2023 10:44:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Mar 2023 10:44:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Mar 2023 10:44:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:44:38 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 10:44:38 GMT
EXPOSE 80
# Thu, 23 Mar 2023 10:44:38 GMT
CMD ["apache2-foreground"]
# Thu, 23 Mar 2023 17:42:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 17:42:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Mar 2023 17:47:48 GMT
ENV DRUPAL_VERSION=7.95
# Thu, 23 Mar 2023 17:47:48 GMT
ENV DRUPAL_MD5=ebd3b1ef8605585d703c13552f841731
# Thu, 23 Mar 2023 17:47:49 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:369fe072796976e1501c1a8d490c05b9ac47287c34c004013e0982d2dd4bb7c2`  
		Last Modified: Thu, 23 Mar 2023 01:33:32 GMT  
		Size: 22.7 MB (22748632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996895293e2c2af33f1bb50acd02b4400f04a4dcf57ddedd68e50599416caf53`  
		Last Modified: Thu, 23 Mar 2023 10:52:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42cb3f50a59194bcc38d67ad256f4f2ea02d33a535cfc4746bfac34a85c8f8`  
		Last Modified: Thu, 23 Mar 2023 10:52:21 GMT  
		Size: 59.5 MB (59543404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf21d7202aeadab485cd99745b4decb146036e7aaac8737d3355b0e017f8564`  
		Last Modified: Thu, 23 Mar 2023 10:52:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf618cd406a3d9aa26189bf26a6dd1fa0581b028add545b12038d07b1003a0a`  
		Last Modified: Thu, 23 Mar 2023 10:52:47 GMT  
		Size: 17.5 MB (17481692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35a73f0d26550e8a93c2d51126a0166093cbe4a1ac6f9beb5bc56336ed6711`  
		Last Modified: Thu, 23 Mar 2023 10:52:45 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07596d7b35761071bc642f77ba3061f9dff257addc2626f4c73e4f81e661212`  
		Last Modified: Thu, 23 Mar 2023 10:52:44 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f762334ef6edb4886ea3ed069a526a82a95a66ac34ac81b914d06ddc9ad8`  
		Last Modified: Thu, 23 Mar 2023 10:57:32 GMT  
		Size: 11.1 MB (11138984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d6b5ef011ef695f695e252448845c678ca2ea6e98f86cc60c6999e4c7085d6`  
		Last Modified: Thu, 23 Mar 2023 10:57:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327db232d7b51d06a051f6d4e7da3a91256f0a703d911d5d1ce57d1ed06be0e1`  
		Last Modified: Thu, 23 Mar 2023 10:57:31 GMT  
		Size: 9.3 MB (9256733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dbec48631d473deefe80966a294271af04d5f538b826b1a1f95c3ccfaef9c1`  
		Last Modified: Thu, 23 Mar 2023 10:57:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c414ab4ce27e9c6f119535b96bedf306f091bcb7c8952470276c84dce6ab4a`  
		Last Modified: Thu, 23 Mar 2023 10:57:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adff79a162ce086182cab4bafd848457d4f25d93f48cc7eeb54a77ebcce2ee64`  
		Last Modified: Thu, 23 Mar 2023 10:57:29 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd05b2d8568de0c770b4f1e7df0b72e4610f8614c6ca624b96286c6c95745340`  
		Last Modified: Thu, 23 Mar 2023 17:57:47 GMT  
		Size: 1.6 MB (1633119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b0df864f39726fc45d3de47c3254615fd1f3b81be85285aa77d1d7a91c1320`  
		Last Modified: Thu, 23 Mar 2023 17:57:46 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4b9c0c8a3b6d50949c02b641572ca40eb6a0c4e0b637f90fcb3ea622af368`  
		Last Modified: Thu, 23 Mar 2023 18:02:33 GMT  
		Size: 3.4 MB (3402770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:bc38051607b8ea6b580c9590926fad1236d072b31c7dab43a70693b1f4af2da1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141524841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336f891d3f6e7b1298d92d24a97a4faed075916dbaf37788d63ce553a26e90cf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:24:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 12:24:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 12:25:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:25:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 12:25:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Mar 2023 12:28:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Mar 2023 12:28:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Mar 2023 12:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Mar 2023 12:28:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Mar 2023 12:28:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Mar 2023 13:12:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 23 Mar 2023 13:12:41 GMT
ENV PHP_VERSION=8.0.28
# Thu, 23 Mar 2023 13:12:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Thu, 23 Mar 2023 13:12:41 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Thu, 23 Mar 2023 13:12:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Mar 2023 13:12:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:14:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Mar 2023 13:14:47 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:14:47 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Mar 2023 13:14:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Mar 2023 13:14:47 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Mar 2023 13:14:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:14:48 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:14:48 GMT
EXPOSE 80
# Thu, 23 Mar 2023 13:14:48 GMT
CMD ["apache2-foreground"]
# Thu, 23 Mar 2023 19:55:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 19:55:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Mar 2023 19:59:17 GMT
ENV DRUPAL_VERSION=7.95
# Thu, 23 Mar 2023 19:59:17 GMT
ENV DRUPAL_MD5=ebd3b1ef8605585d703c13552f841731
# Thu, 23 Mar 2023 19:59:18 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d986ff4e4cf97a42b83fd9c83a28cd860ad9466daad20f215ac4148673a58052`  
		Last Modified: Thu, 23 Mar 2023 13:22:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb88fcece1e9a98713860e0048b95dffe1a07d8480d365491a749fb1dab1ce`  
		Last Modified: Thu, 23 Mar 2023 13:22:33 GMT  
		Size: 70.4 MB (70365819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d88f9e53082155e46ba1806c06508e8e86a204eac61d69b95f1340ca74d1a`  
		Last Modified: Thu, 23 Mar 2023 13:22:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f4fed24c0975b0ed9c475b52dc64798b18909fc45b1ff496d44c2ca203735`  
		Last Modified: Thu, 23 Mar 2023 13:22:58 GMT  
		Size: 18.6 MB (18585841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4713c9f3df8c793d45bd52f2649ca1c46c8c8f4e7f00e2366c0c69b9081e5ec`  
		Last Modified: Thu, 23 Mar 2023 13:22:56 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac5ce312fb6c8c8db4227d097a61da363efea342381b76d848703b8f428ed98`  
		Last Modified: Thu, 23 Mar 2023 13:22:56 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b58c9736d65b46ec5a581de85884200ca3fc35219225cffcd39b122cddc6aeb`  
		Last Modified: Thu, 23 Mar 2023 13:27:33 GMT  
		Size: 11.1 MB (11139790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf36c92d9e23f96778bf432ad369e4d4223c782d9779ee2f52b46fb8c7024ff9`  
		Last Modified: Thu, 23 Mar 2023 13:27:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211554c5d5d5e78f355f91b0a6a14c1b7152bb2135c9a94f850b45e544af1329`  
		Last Modified: Thu, 23 Mar 2023 13:27:32 GMT  
		Size: 10.2 MB (10201827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700b73e6e35870b1635557cb1834f6512bffa55f8f746bd7a1210b319e080858`  
		Last Modified: Thu, 23 Mar 2023 13:27:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c789ad105f24a173946bae3602cc5d6c05479f478d6643e302e2bbdf0539a72`  
		Last Modified: Thu, 23 Mar 2023 13:27:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb84c79ffd4bca9612dc0ce9003b90c1733024d0cbaba06f5a82d07ffca7229`  
		Last Modified: Thu, 23 Mar 2023 13:27:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937eb8368261b67f00abaee52e21fb231aa669b457d441a26de532195be60488`  
		Last Modified: Thu, 23 Mar 2023 20:08:26 GMT  
		Size: 1.9 MB (1900266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2033487bf9346520fba2ae3220c7d6348f5a13ef9c609736be3e86574b7c9ffc`  
		Last Modified: Thu, 23 Mar 2023 20:08:26 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c0829218e04e246c8d30e056557fb5e869431c61eb0b25e14d1b7eb5821934`  
		Last Modified: Thu, 23 Mar 2023 20:12:38 GMT  
		Size: 3.4 MB (3402765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:43bc9898cb08ec0357bf5898ff320c578c1333d9a441591f5f9116cef144f1f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9858ba05fd0e4b92fedba91d611314b2d736fd39396f41b005666900eac0b5f3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:35 GMT
ADD file:d90e1c78fceb91ea00c9b00cdf477b7254e3d4d37b561698e90b75c62d84320c in / 
# Wed, 01 Mar 2023 01:39:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:47:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 01 Mar 2023 14:47:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Mar 2023 14:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:47:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Mar 2023 14:47:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 01 Mar 2023 14:52:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Mar 2023 14:52:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Mar 2023 14:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 01 Mar 2023 14:53:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 01 Mar 2023 14:53:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Mar 2023 17:36:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 01 Mar 2023 17:36:19 GMT
ENV PHP_VERSION=8.0.28
# Wed, 01 Mar 2023 17:36:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 01 Mar 2023 17:36:19 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 01 Mar 2023 17:36:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 01 Mar 2023 17:36:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 01 Mar 2023 17:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 01 Mar 2023 17:41:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 01 Mar 2023 17:41:03 GMT
RUN docker-php-ext-enable sodium
# Wed, 01 Mar 2023 17:41:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Mar 2023 17:41:03 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Mar 2023 17:41:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 01 Mar 2023 17:41:04 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 17:41:04 GMT
EXPOSE 80
# Wed, 01 Mar 2023 17:41:04 GMT
CMD ["apache2-foreground"]
# Thu, 02 Mar 2023 07:04:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:04:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 16 Mar 2023 00:52:46 GMT
ENV DRUPAL_VERSION=7.95
# Thu, 16 Mar 2023 00:52:46 GMT
ENV DRUPAL_MD5=ebd3b1ef8605585d703c13552f841731
# Thu, 16 Mar 2023 00:52:47 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:5dd0dee7d259a761fe8021e1fd6a2a9a8590880098b27d4f97cfbda4e50bc631`  
		Last Modified: Wed, 01 Mar 2023 01:45:36 GMT  
		Size: 27.8 MB (27798766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c6bf19cab4ac9a56c078c6948c57f559d8d6a8188a9f8479f1a3ba2d7cdbd`  
		Last Modified: Wed, 01 Mar 2023 18:21:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c1ee9425978cc9dee96402d220271f287bd024f8e3f70b60b45e54626ad6d`  
		Last Modified: Wed, 01 Mar 2023 18:22:13 GMT  
		Size: 81.2 MB (81238084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a0778af02b444a917ecc9c784e60e3f0600ac5b79779d0c9c45fc5142d06e3`  
		Last Modified: Wed, 01 Mar 2023 18:21:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28022b3a19c3b0e511a813ff76da4dd9249618ded71866118b549444a54dd9d2`  
		Last Modified: Wed, 01 Mar 2023 18:22:48 GMT  
		Size: 19.1 MB (19116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110aa2434c6ea7bd36e9a6545e39bd768d2632b85686d39f94ff6c99a3db4a9`  
		Last Modified: Wed, 01 Mar 2023 18:22:44 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90394f28f547516f93afb2b3de5e8896544b6b0d7e2cc802f3e2a5910ae99cda`  
		Last Modified: Wed, 01 Mar 2023 18:22:44 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce379a90573e88aaf48d90d2f9ef2391864be10cd561f01e71a22e97d06c7269`  
		Last Modified: Wed, 01 Mar 2023 18:33:54 GMT  
		Size: 11.1 MB (11140404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00852d403fab0496be1a4e497996565cc014023cbbc497ae95ce4c917491247e`  
		Last Modified: Wed, 01 Mar 2023 18:33:51 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaed44ad98d2febab09613c8dadec125b9701cd38143449624264115ff364a51`  
		Last Modified: Wed, 01 Mar 2023 18:33:54 GMT  
		Size: 10.9 MB (10937711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72726d498dbc1b9c674306e91cc09c9d4a26f2347e6840f6fb02b4bff82e6dfe`  
		Last Modified: Wed, 01 Mar 2023 18:33:51 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7bbfb93907a648c4ee58658f277a504d442b64feddcbbb07c13cb40aae29a4`  
		Last Modified: Wed, 01 Mar 2023 18:33:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89c9cdc4e226951afc3500f319461549357f331e680f4fc012b706228ab92b5`  
		Last Modified: Wed, 01 Mar 2023 18:33:52 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525f4fb39d134bdd7164c03d25f0f57f6006e46526b2c88112dad538d892f1e2`  
		Last Modified: Thu, 02 Mar 2023 07:36:24 GMT  
		Size: 2.3 MB (2316573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df34046dfcaf0771748d8e2d49e67e7399ac96052792706c566d1ebec3cdbce`  
		Last Modified: Thu, 02 Mar 2023 07:36:23 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cde357e70516ec230797b6ce0b66be1ab708b86868c59a90d49947a1de99414`  
		Last Modified: Thu, 16 Mar 2023 01:26:45 GMT  
		Size: 3.4 MB (3402780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
