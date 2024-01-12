## `drupal:7-php8.1`

```console
$ docker pull drupal@sha256:21016f799fdfb03196bc0f294f982ecbf449c9d5762c65d00152b17e19a9329c
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

### `drupal:7-php8.1` - linux; amd64

```console
$ docker pull drupal@sha256:6228e35cceb4b81ad0cf0ea400f54d5a70bb530a0a51f72b621379fc294c37f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182607632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8875d6660095b67a322a362797980134ef69e894ea237d20e0115555ea9155b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a95dcec60350663284915f66e96b2d216179ebe405663a818c81de0f22f45e1`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22afa33f327082e95c674a5bdf3b6d25760aca5abce3b032de2c444ba4864ed`  
		Last Modified: Thu, 11 Jan 2024 08:45:06 GMT  
		Size: 104.4 MB (104352766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa61ea11ee8a864fd6b368bd09be18de3692f7ada24f03df32e585107432160`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ae2bde3303f6e68d4e0f2e641771894224010749cd780d5b602f500d3c81`  
		Last Modified: Thu, 11 Jan 2024 08:45:32 GMT  
		Size: 20.3 MB (20303737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5356c6468fd18c3e8b9c7b77f02d4387bc52f207263ad1766a141711da8b02`  
		Last Modified: Thu, 11 Jan 2024 08:45:29 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91cb51e8865de77fe278c43f87cd11246e5a71d43047c7be581b1475e1cd31`  
		Last Modified: Thu, 11 Jan 2024 08:45:29 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594d91baae92d9258db2c2df04e7a468538225309761e184872baf18d6d1a74d`  
		Last Modified: Thu, 11 Jan 2024 08:56:43 GMT  
		Size: 12.2 MB (12247899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69351fc82abb78afae491167773b6799bac45f0a213751d37e4f592336685fe`  
		Last Modified: Thu, 11 Jan 2024 08:56:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faa4420ad83ed3cb1e0b21f2d83da6f49496b9aa1dffe63ed077a7b0542575a`  
		Last Modified: Thu, 11 Jan 2024 08:56:42 GMT  
		Size: 11.2 MB (11156649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7f7f06a3a9a913a5f7352f2f9b0d22618ccfd398a7296e2305c073719a1718`  
		Last Modified: Thu, 11 Jan 2024 08:56:40 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c5e6b395df54adef7dabca1c92ffa201174325c18342efda8b42889e423fe`  
		Last Modified: Thu, 11 Jan 2024 08:56:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f25084bacad640f573afe1a7e573bea22f11525da21702a586bed5ecc469c7`  
		Last Modified: Thu, 11 Jan 2024 08:56:40 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d3fb78e0ec12b6e1f5f92d8416979838729cf8dbb8f0e11612d804fbfa5e6`  
		Last Modified: Fri, 12 Jan 2024 00:21:09 GMT  
		Size: 2.0 MB (1995899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3578d36e42d47e52acf218b027c6e13f2bf874971d4cfbafc710902635e4e`  
		Last Modified: Fri, 12 Jan 2024 00:21:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40ec7214d8b578370f3173fe633a7013ef68b2190bde3789dcfe650e6c304b8`  
		Last Modified: Fri, 12 Jan 2024 00:21:08 GMT  
		Size: 3.4 MB (3418881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:b340065830e9903171c36745a9f5f0a78154a033a5d7f060a6e55a4a8952051e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d2b539df8899fa5fd7d0bb424bfc669b342918d2751667f9a59238e7345d52`

```dockerfile
```

-	Layers:
	-	`sha256:f33c6834c6ab7f4a9e43bd4d48f6d2e2b36348c0a88748af720d401fa036593f`  
		Last Modified: Fri, 12 Jan 2024 00:21:08 GMT  
		Size: 5.9 MB (5866132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e96cd561293303a5a0b4c168c3d00aa2b2d9cd22ebe31b4297545d0dc583a5b`  
		Last Modified: Fri, 12 Jan 2024 00:21:08 GMT  
		Size: 29.9 KB (29892 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm variant v5

```console
$ docker pull drupal@sha256:b2c3415099a1f34b7de6e7f94a0324e3f12e1d865730631048b538ffcfa6f232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156220351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f10629f316facf232ef27c99762c55cba03a9cfceaaee9bc37809a5c68746a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:18:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 02:18:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 02:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:19:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 02:19:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 02:22:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Dec 2023 02:22:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Dec 2023 02:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 19 Dec 2023 02:22:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 19 Dec 2023 02:22:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 19 Dec 2023 02:22:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:22:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 02:22:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 04:01:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 27 Dec 2023 23:39:17 GMT
ENV PHP_VERSION=8.1.27
# Wed, 27 Dec 2023 23:39:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 27 Dec 2023 23:39:17 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 27 Dec 2023 23:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Dec 2023 23:39:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:46:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 23:46:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:46:42 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 23:46:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 23:46:42 GMT
STOPSIGNAL SIGWINCH
# Wed, 27 Dec 2023 23:46:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:46:43 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 23:46:43 GMT
EXPOSE 80
# Wed, 27 Dec 2023 23:46:43 GMT
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
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34b73d2d8e6b1b2c10c6eb4b942988f6ab53d0815dcfbc221d087c716a8b22`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c7dffc50fc2b8f2714576406c9c543112a528c0e55e72bb5dcd48e02d697ba`  
		Last Modified: Tue, 19 Dec 2023 04:48:08 GMT  
		Size: 82.0 MB (81999515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cdf3a474021cac2a6c3b988a5a48cf4a73327b3205a3ba51d644f6035b4456`  
		Last Modified: Tue, 19 Dec 2023 04:47:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddaddfc8f048c69c45769fae6c7545f575b88ca39d32f7e745157aacfaefe3`  
		Last Modified: Tue, 19 Dec 2023 04:48:35 GMT  
		Size: 19.6 MB (19608241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97e438b6275096e6d3a330b3d49be2ece9486d7bb206bea33328ce2364eaa6f`  
		Last Modified: Tue, 19 Dec 2023 04:48:32 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298b2a8ea271468b38aed2074dec7c9ef02c04bf65e903e14b264641f3ca2ff5`  
		Last Modified: Tue, 19 Dec 2023 04:48:32 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14001dc8ec2814eba15e233ef5739a2ce1ef36a70d40cf6d5409eb0bd9f31c55`  
		Last Modified: Thu, 28 Dec 2023 00:38:14 GMT  
		Size: 12.2 MB (12245914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad5007734cd58b0c66e24f7bf61adff179744c659c7b3c36d1e37563cf89d3`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a4eb4f1d09dbc769d915a6d01a0ef4b91ed7eb8a17faafa2437b04169b544`  
		Last Modified: Thu, 28 Dec 2023 00:38:14 GMT  
		Size: 10.6 MB (10593991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbd06163cd5e58e925dc7844872e89138ce83e1fb4369f0729116a642eafee3`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caee4d7320dddda3e8c9d7d7d9e788edc5b9fbd2e7167e65a66c82f0bfe758c`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf6ff1c00544cd117c02c17fdd17a438ad777f9aa67e2eb5e84473684efacfa`  
		Last Modified: Thu, 28 Dec 2023 00:38:11 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d9b6fe932347d958ddf888fb1463d97177fa007f385f5c1efc404486ace22`  
		Last Modified: Thu, 28 Dec 2023 04:09:07 GMT  
		Size: 1.5 MB (1462468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2e90812fff864c17040521dc5523e308080d34c27f7fd0300975b24c9707c9`  
		Last Modified: Thu, 28 Dec 2023 04:09:07 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5025f5ee119e1f52ebb00de59ddc44d35c81bc06487a5146a0d89d67481a348`  
		Last Modified: Thu, 04 Jan 2024 01:12:13 GMT  
		Size: 3.4 MB (3418881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:e66c46d2ad319f40e64e1cacbd41ca28f3719c129b9ea1dc7031d450c21f5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5729752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16fb869279cae8a3bfb1c220a5cf22c37acfa99ddb725d4d52a6e831d9e476c`

```dockerfile
```

-	Layers:
	-	`sha256:ee5bbb91d8e37b3257a01cf444c063a22048b6f52c1097ab1e5adb8e3c0ad8a6`  
		Last Modified: Thu, 04 Jan 2024 01:12:13 GMT  
		Size: 5.7 MB (5701813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a45296804f14517194bfbb8626a4a41adb0382a11782d04ed85458037c68c3`  
		Last Modified: Thu, 04 Jan 2024 01:12:12 GMT  
		Size: 27.9 KB (27939 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5f592411a3c22d308b17b190174bcc9365341053d27489357dfbc58126c6b10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146971251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec5c6a64297335c3fa5172b28787dd6bd0a1379b680f323fed5c00f4f91ca11`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:50 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Tue, 19 Dec 2023 02:07:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:09:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 05:09:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 05:10:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:10:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 05:10:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 05:13:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Dec 2023 05:13:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Dec 2023 05:13:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 19 Dec 2023 05:13:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 19 Dec 2023 05:13:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 19 Dec 2023 05:13:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 05:13:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 05:13:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Dec 2023 06:48:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 01:28:58 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 01:28:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 01:28:58 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 01:29:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 28 Dec 2023 01:29:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 01:36:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 01:36:20 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 28 Dec 2023 01:36:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 01:36:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 01:36:22 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Dec 2023 01:36:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 28 Dec 2023 01:36:22 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 01:36:23 GMT
EXPOSE 80
# Thu, 28 Dec 2023 01:36:23 GMT
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
	-	`sha256:65ab19615c01a3b542f77fadb3bd27872b6a20cba3e9269fb951de36d8fa6805`  
		Last Modified: Tue, 19 Dec 2023 02:11:52 GMT  
		Size: 24.7 MB (24718157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65740699e811c46b300dc1c124377acd0b62ad6293d766b800ff0b0b1b15ee4`  
		Last Modified: Tue, 19 Dec 2023 07:35:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec00c82ca03d32d2179c766fbeb2791d1a6a7104cd30a45449f41afb3f0330b`  
		Last Modified: Tue, 19 Dec 2023 07:35:33 GMT  
		Size: 76.2 MB (76167957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0665bd380315b2d7d72a79a178c0632e460bcca310ce7a4d22f72d74308b66`  
		Last Modified: Tue, 19 Dec 2023 07:35:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87e8e176db52cf02bbac190df26c2b5b2d182d6fc422d729b45cbbd4dc7d955`  
		Last Modified: Tue, 19 Dec 2023 07:36:03 GMT  
		Size: 19.0 MB (19045352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e9c21e2f8d836c54fb9350565c794082c47ae434dd3144be72fc15ac3a9279`  
		Last Modified: Tue, 19 Dec 2023 07:35:59 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1927f0f803b500e6a170c314fa969007b5682fd1ffd745f1de74bee82a931f0`  
		Last Modified: Tue, 19 Dec 2023 07:35:59 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed6cac110eaa072c8e54e24f2f72e71067c3ff3d9b3b491e328cf0ff91012e`  
		Last Modified: Thu, 28 Dec 2023 02:56:04 GMT  
		Size: 12.2 MB (12245895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f2521d0131b12aee553634bc0a77264e8efbb7b3149fca19706f98c143482`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d56039f6425053b12d7803ddd97b1fada42f38d231f8b8103bfa536ed22a63`  
		Last Modified: Thu, 28 Dec 2023 02:56:04 GMT  
		Size: 10.0 MB (10024261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd9439b47c9f4ac2e616965544c53e73452f74aa3970316b30d9a7beeabe3d`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8cb315c8b7dd28eb7710cf655501a11877dce475a404e9e113b90326529182`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f23331ad58108ec19356a3e7682be534465c5764fe439d39cb7c782523db06`  
		Last Modified: Thu, 28 Dec 2023 02:56:01 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e946312da6c557bbde1f87e5681dcda9f33c3395ae6aea12f961f692b00417`  
		Last Modified: Thu, 28 Dec 2023 08:51:09 GMT  
		Size: 1.3 MB (1344852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be10f0607b62c43db6d33b2173489ce4f9254f35b8df318bf064621338691502`  
		Last Modified: Thu, 28 Dec 2023 08:51:09 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728adf89f125f1dfb7f8570a5b5875e7ade29ccb757f4c7c4a7f596516d60072`  
		Last Modified: Thu, 04 Jan 2024 01:54:24 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:a20afb2632c11660f4e7ff2af9330f493ce8f56464695a876f2a1e96e6bae5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bed11c162e2adbf36ca7119bcf186fea6a1dd219e5f246394642a99abf0c4c`

```dockerfile
```

-	Layers:
	-	`sha256:b7aa61e35a916f66c8d28202227c6ad8f2f83362973fe981e03810b098e3093e`  
		Last Modified: Thu, 04 Jan 2024 01:54:24 GMT  
		Size: 5.7 MB (5705799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29eb6e5f74d1a89f2927f072cb13a23abfcb6d413e377399ec5b8b7872088da`  
		Last Modified: Thu, 04 Jan 2024 01:54:23 GMT  
		Size: 27.9 KB (27939 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:b13ab7c4e6315d3c159cafeed32c74caf11fd6a219598785631ae4fa9ba0dc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176669560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5af70dab494f5dc34bd6210024c848babf5cd1c77f30034bc70db6315d1b8d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451161081bb50dfa3757568668f099cf58479733644abdbc5c2f79d7c4d9cade`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e283d29837ef0a320a5446924b58fe28a48bdb544e3b65cc753b44483e58aa4`  
		Last Modified: Thu, 11 Jan 2024 05:46:13 GMT  
		Size: 98.1 MB (98128972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99cfb51d5dc36e05dbed790e970497125214a08a60c68ef185661b1a6638e4a`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762abba6396b86cd8ac66ebd05371dfddd5a4be381c99d663cfd880c4c32c5c`  
		Last Modified: Thu, 11 Jan 2024 05:46:40 GMT  
		Size: 20.3 MB (20305032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269b42eeb2e3e56c31a41df02e0fd99dda0c92189c542f90f69f5aef4b538b5`  
		Last Modified: Thu, 11 Jan 2024 05:46:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612f169f08b23d156c839c07adbdf6aeede1e477b8a1745a92f0e501405d955f`  
		Last Modified: Thu, 11 Jan 2024 05:46:38 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d702d6838bea83a5606825c515846e29ba2eeee12c40612bbb9eeb69f2df18a`  
		Last Modified: Thu, 11 Jan 2024 05:57:08 GMT  
		Size: 12.2 MB (12247560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43ba5f0c54f21e8af3a5e2aa0672922c462d95746b6f0ed949d625e1f05eaeb`  
		Last Modified: Thu, 11 Jan 2024 05:57:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fd1e794ba5b067c98fe656bd0d1aceb3d28db9b7a640252d456e9f3af9da1e`  
		Last Modified: Thu, 11 Jan 2024 05:57:07 GMT  
		Size: 11.2 MB (11151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9befdc89a9efc098676d6d69f7079567d442cdd9a4f329de698687b95e6eb7d3`  
		Last Modified: Thu, 11 Jan 2024 05:57:06 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6c80abde7ec8274f0993e93ec4843e25cdd6f8738cdf1b32570785624b3f1`  
		Last Modified: Thu, 11 Jan 2024 05:57:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e9fffc2e818cf8ff9236d3f49d907a8bf65462020b4e49bc7213410f81c8a`  
		Last Modified: Thu, 11 Jan 2024 05:57:06 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f888c542aaa49fc170c8107dedf1027c640fdfc72fa8ec937c5db92d7fbfb60`  
		Last Modified: Fri, 12 Jan 2024 01:23:31 GMT  
		Size: 2.3 MB (2254185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bee5621742219cf153fc75c7ff760541e22e66fe3445c7168598c9bf666244`  
		Last Modified: Fri, 12 Jan 2024 01:23:30 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954f6d870534791cd799ce7f5ec5ef87c35fd69d4f5576b2275d68dca0b54aeb`  
		Last Modified: Fri, 12 Jan 2024 01:31:49 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:923df83ea5ec4780497449b4644201dc33206f050ed9e55b30366f73318bfaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5918960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745a4c4c801c587a2b88d8e5f80476dd2dce4789fc054d543b5a79a59136c99f`

```dockerfile
```

-	Layers:
	-	`sha256:7ffe01dcc9cd45151209d0eef3ec35d4b0abc3e405413cc4f0398f295da88ddc`  
		Last Modified: Fri, 12 Jan 2024 01:31:49 GMT  
		Size: 5.9 MB (5891155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c938eaba48f5f73b707db3de3eece01e58af03e01c01a33b4a226fe3ba60f9`  
		Last Modified: Fri, 12 Jan 2024 01:31:48 GMT  
		Size: 27.8 KB (27805 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; 386

```console
$ docker pull drupal@sha256:c6972808d18419ee4e3c56eede04404125868134af349edb01202d527d9f4fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181603594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3fbb3ea6d2e31b5db6d5463626021956837d17593398d403bdd26d453c31a7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946df82896e7966597c6491529e0230dd6f4ba0b305c589840bc9133f0535fa4`  
		Last Modified: Thu, 11 Jan 2024 09:11:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76d33e770c7aaf9e80071255e0e21cfc96139d4398eeda332ed50d769a3e6b0`  
		Last Modified: Thu, 11 Jan 2024 09:11:46 GMT  
		Size: 101.5 MB (101534598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97c877b297ab5b95038cd30ec523bacef9b483ba3674f3ddf56597062ef9955`  
		Last Modified: Thu, 11 Jan 2024 09:11:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0b6736627858a695eb9b48b55ce6ef151a47aae0f60810d77efb68928bc15`  
		Last Modified: Thu, 11 Jan 2024 09:12:15 GMT  
		Size: 20.8 MB (20825996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c39c6532ba583bb00f0f880fa1ec094d1dd2e8e9a00e933b12731b486b3db7`  
		Last Modified: Thu, 11 Jan 2024 09:12:11 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9ecb92d7ef9c250277fa01c18fa30461213a07d580f494d2e70daaf794d7a`  
		Last Modified: Thu, 11 Jan 2024 09:12:11 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c8a5f6280d2779043a6fe5a5bed55196b437b82afe774fdbf3aeabc45f8236`  
		Last Modified: Thu, 11 Jan 2024 09:24:47 GMT  
		Size: 12.2 MB (12246931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076d2e336448f11a7144ee0be954f0baa62a51a076db675f40be12873a6f2897`  
		Last Modified: Thu, 11 Jan 2024 09:24:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b5787df19bbbc94545a9c074dae48693ea91bd417394d3190a6f2e982912f8`  
		Last Modified: Thu, 11 Jan 2024 09:24:45 GMT  
		Size: 11.4 MB (11379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091d917ff8cfca19afd9a4fbec1c6fc38e144b454d8e646127c5cce7cc60497d`  
		Last Modified: Thu, 11 Jan 2024 09:24:41 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ce4dba1e8ddb9478fced3be88c803c80abfd3f6e53bb6d6b177ce6c4c1fe9a`  
		Last Modified: Thu, 11 Jan 2024 09:24:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126f023877cff7c2d4a2962abceade6679dd24be937b7d5fab2de8da72e8bc3e`  
		Last Modified: Thu, 11 Jan 2024 09:24:42 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10493deda5814b0fab256faad1ef753df133390b3b6860310fc7024f732d228`  
		Last Modified: Fri, 12 Jan 2024 00:21:09 GMT  
		Size: 2.0 MB (2047944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6702b700672d60574fc298622e0fdf1afcd873380b9defd9392a97843d965`  
		Last Modified: Fri, 12 Jan 2024 00:21:09 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0937c53a1b180e4c31fe4a6ace06dcb505290c53f5061bc3c875efcd124ce9f2`  
		Last Modified: Fri, 12 Jan 2024 00:21:09 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:3f0ef26902359b374a90d91ffb5faa6f66f060f40ceca10d23ff7ec5277ee01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff68121c04994036f77f011422081c6ceffb79b5cc7efdfe7c1e79ae14482cc0`

```dockerfile
```

-	Layers:
	-	`sha256:5817c6a65280bf77bc76d2969d5d443208600b028f70f72fc7572351f9d3dcd9`  
		Last Modified: Fri, 12 Jan 2024 00:21:07 GMT  
		Size: 5.8 MB (5848228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4faff4b2939f179b63df7e260dcce145635d5f2ebe5deee86ce3ef7aec137e`  
		Last Modified: Fri, 12 Jan 2024 00:21:07 GMT  
		Size: 29.8 KB (29819 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; mips64le

```console
$ docker pull drupal@sha256:464bea1169cce2fe34e130ac5ab469917940a2c9664d0b535f9acb4605f16063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157592301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a15c9f09da39a74a1b083e2848fc7af6427e91330c04418f3130fcc526604c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 19 Dec 2023 02:13:36 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Tue, 19 Dec 2023 02:13:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 19:30:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 19 Dec 2023 19:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Dec 2023 19:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 19:32:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Dec 2023 19:33:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 19 Dec 2023 19:49:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Dec 2023 19:49:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Dec 2023 19:50:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 19 Dec 2023 19:50:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 19 Dec 2023 19:51:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 19 Dec 2023 19:51:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 19:51:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Dec 2023 19:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Dec 2023 04:06:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 02:32:04 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 02:32:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 02:32:11 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 02:33:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 28 Dec 2023 02:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 02:48:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 02:48:30 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 28 Dec 2023 02:48:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 02:48:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 02:48:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 28 Dec 2023 02:48:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 28 Dec 2023 02:48:49 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 02:48:53 GMT
EXPOSE 80
# Thu, 28 Dec 2023 02:48:56 GMT
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
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff381284c38c37d044a037404bee595ddb632e19af4a73c9058bea92695edbb`  
		Last Modified: Wed, 20 Dec 2023 07:56:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edab9ad60196317b7f02dfcef36f9ad767f6874b4de61ca1f73fab286d082fb3`  
		Last Modified: Wed, 20 Dec 2023 07:57:17 GMT  
		Size: 80.7 MB (80667789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3523b846b656b447f978cf98633f848ecc8faf559395c2a42429df15228ef3f`  
		Last Modified: Wed, 20 Dec 2023 07:56:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bd9b49ee2f2c9ffd8c228cc5e88d4b269d7580e1466a8e569d92f72f259a9e`  
		Last Modified: Wed, 20 Dec 2023 07:57:58 GMT  
		Size: 20.1 MB (20053889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b188605258ed68260d81033659d0de0109c45d7a018eb667017a329ec48ebc8`  
		Last Modified: Wed, 20 Dec 2023 07:57:44 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d86fcf97450d81fdfeb49958420896ee40c5d50d6dc6ab326588a3b7ec4f125`  
		Last Modified: Wed, 20 Dec 2023 07:57:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea1bdf930db5ef10c30e36c0175eb078d63cd1e5fff1bfd282725d4348807d1`  
		Last Modified: Thu, 28 Dec 2023 04:29:30 GMT  
		Size: 12.0 MB (12041223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf1aa0789fb562c778c0b78811622c5fa4f80039cb17ac2639767c38d464bc9`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1d25faa45e95f013fba3d4a0d6ef89949c99a0314cf2daf5d9609bf318f4e`  
		Last Modified: Thu, 28 Dec 2023 04:29:33 GMT  
		Size: 10.7 MB (10718553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89211ee7aa0ff3c668842e92dffb9e3cd0d8629b05d327d2584cf1933d493945`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251c00248b2289745f68e003d4a47aad4f2b12fa987eafad5f14e5dd4164e8d2`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743b008ecf8d08ed839b0a3c1ad39aeb51578450a2802559b204187dcbedd778`  
		Last Modified: Thu, 28 Dec 2023 04:29:25 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989dcb3f328d377a905b6e9062912910110e16b35889af341287ba38eaa2a266`  
		Last Modified: Thu, 04 Jan 2024 01:17:28 GMT  
		Size: 1.6 MB (1564734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dba6decb83b0d9b9d5a8450c33b8248b70af7564089855bd47fb78fb9905b03`  
		Last Modified: Thu, 04 Jan 2024 01:17:28 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118e9ebecc55b448f663f1ac42a9735ad3997cf103210e968632334a41e508e`  
		Last Modified: Thu, 04 Jan 2024 01:17:28 GMT  
		Size: 3.4 MB (3418882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:64c1a87b3a228c6c23cff6d9aed11004d88cc07df442765e2a93581658fa969b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 KB (29807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc92473ddfe8f15e7454beaae96e025ee40bb0ce05581b5b5c75925d299cc427`

```dockerfile
```

-	Layers:
	-	`sha256:900266659debfe0290d7ce36da11abb72f158ade9ea9fffe01b23bc828798f04`  
		Last Modified: Thu, 04 Jan 2024 01:17:27 GMT  
		Size: 29.8 KB (29807 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; ppc64le

```console
$ docker pull drupal@sha256:74ecc0d03265ac9f5118db5dd762d46bb308bc0e5bcd49fe171ba6420ccc7604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (186978909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9afdf5e53fe82a09257496910b682dbe1ad5769c3d8283165d0d151a1e54a3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deccbdb3118a70cea029f0aa9a00e20f50a0f9e7ee48c0b2e47e908baa1aa9`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b1fe163bf5146471d387e12d2994c0200954be8c29360da9b7d6645856db5d`  
		Last Modified: Thu, 11 Jan 2024 06:47:21 GMT  
		Size: 103.3 MB (103321106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21810f5c2e4eb5e038fb75e5935cd7ee106a1f1c2af8465b5b414700d1cbc42`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db359f0198220811583d45f054d34f3c7eece5487a08c02682858796dd467dcc`  
		Last Modified: Thu, 11 Jan 2024 06:47:51 GMT  
		Size: 21.5 MB (21489342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b50b7700af076c4027ca4685d067048893bbd5b852047f87dbaeb97568c66`  
		Last Modified: Thu, 11 Jan 2024 06:47:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e9665480e2e5dd3d7d2c11091468a75255d8bdaec9cc796844f121e83048f`  
		Last Modified: Thu, 11 Jan 2024 06:47:48 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d71e95b1b3bb8a245e68fcc5d1f2d426fe61d5ef7e67d67375b497d4dc4cb7e`  
		Last Modified: Thu, 11 Jan 2024 06:59:58 GMT  
		Size: 12.2 MB (12247274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c40c3fa5a42e4302d6a1e9add78eaac94fcc8d10dfe7d6a50707f59e2ce9bd`  
		Last Modified: Thu, 11 Jan 2024 06:59:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04619949dfdc11124af2ada01a3ac4ac8696aa4c27ec964a0a62a2f5caad152e`  
		Last Modified: Thu, 11 Jan 2024 06:59:57 GMT  
		Size: 11.5 MB (11526816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c480efe61f3a4d71b168d7e27750060784dfc447d933172bd53e5e0aa75c0c`  
		Last Modified: Thu, 11 Jan 2024 06:59:54 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de582b98f037b1148726a46e929aecd98128a4d82288506e2b7c0bbb252b8dc1`  
		Last Modified: Thu, 11 Jan 2024 06:59:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97bdc02a329e40d3c5457a2b0149efe5b44f0ce0a5bb21464653d13725098fb`  
		Last Modified: Thu, 11 Jan 2024 06:59:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44e4e451abd71e24b935b7e72d7e17620572fefe653349e8960ca58bc14b6d6`  
		Last Modified: Fri, 12 Jan 2024 01:20:13 GMT  
		Size: 1.8 MB (1849054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d619c24ef4f92d0b725f1210ed6d4eb2eb57f8fffed5bfef9d95cf0fd2908`  
		Last Modified: Fri, 12 Jan 2024 01:20:13 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636ebb3cdb64c5952c454170942d2785e095939898a81d730cedf85860ac787`  
		Last Modified: Fri, 12 Jan 2024 01:32:37 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:782e279fdcab1e49c0a87aa64589854911645e1d64f5ed26db1c2fed6136979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925286d89e0b3a112273e279d5dd7706d610c2ecd8544565d836d3d5e6427791`

```dockerfile
```

-	Layers:
	-	`sha256:f5cd5607ee91b0d892c8ba2d75aeb0b692c6298ccdb669af63ddbcf4de3de591`  
		Last Modified: Fri, 12 Jan 2024 01:32:37 GMT  
		Size: 5.8 MB (5847507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696902754610f133bdaec15a01911968d2628a0018e13c5147d6ea6767aec970`  
		Last Modified: Fri, 12 Jan 2024 01:32:36 GMT  
		Size: 27.9 KB (27872 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1` - linux; s390x

```console
$ docker pull drupal@sha256:e7c12b7284237b9d1f9629cf55fc9dc97ab71d17a6791a481380703e2b3b525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155820018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838585506fddb27aeba01211681801eb3e274c978b9fef959bb427714b23b5a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
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
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b99384646b14a68f58b4d5f20aa7646bcdb273987830ab94a7d0c52118696`  
		Last Modified: Thu, 11 Jan 2024 08:18:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937e142a80962f22503718b83e94f9fcb8d1c62fac80dcce04bb7b4061486ba`  
		Last Modified: Thu, 11 Jan 2024 08:18:23 GMT  
		Size: 80.8 MB (80814132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ae514a5d8229351dc8ed615a4b5ab3427359d88b93956cdc894c5a4a652bd`  
		Last Modified: Thu, 11 Jan 2024 08:18:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b8e435e581d3dc2f630e33354f40c1595733614e874fe5325c916b9c05987b`  
		Last Modified: Thu, 11 Jan 2024 08:18:40 GMT  
		Size: 20.1 MB (20083203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77340e1ba61c24de6634913db72d5a424d3864312ac9e0f791c0d19940f708`  
		Last Modified: Thu, 11 Jan 2024 08:18:37 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d4aaa5dad250c12a0dcca6b3b73e0d7c6e5bb321be4a2c64e9a50fa7f9bcda`  
		Last Modified: Thu, 11 Jan 2024 08:18:37 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d7ca6c1ae2d74c05ed75254bba8a048f85e62818ac40a0d05f814fefcbc50c`  
		Last Modified: Thu, 11 Jan 2024 08:26:42 GMT  
		Size: 12.2 MB (12246097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a383946d7d28c358fd4becbe725a9fe4e0ad972203e96fb78339c45f03027c3a`  
		Last Modified: Thu, 11 Jan 2024 08:26:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce87a838a28e9f659b6fd73ac8d342990bf554e3ffd0cca2ada38244750d9fe2`  
		Last Modified: Thu, 11 Jan 2024 08:26:43 GMT  
		Size: 10.2 MB (10213676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ec339f496775b1775d343687456a841d4797e2f3a6c8097ed7902471ff138`  
		Last Modified: Thu, 11 Jan 2024 08:26:41 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bb780ea97ce453f24c2532c568de5ea7dac7a88600586ba9462ae112dee3eb`  
		Last Modified: Thu, 11 Jan 2024 08:26:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c3a8f85f845f268d9e688bee0f18b585fb8ef0f11d9f5857586c779655cf7`  
		Last Modified: Thu, 11 Jan 2024 08:26:41 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146c4c5947b60c028fc849eeeb31986fb378561ae01f83d5d6bd28bf86054bd`  
		Last Modified: Fri, 12 Jan 2024 00:42:54 GMT  
		Size: 1.5 MB (1546303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b775f211cb17cd6375f07d4bc8691d316857b68fb5addec23b9e182fdece9871`  
		Last Modified: Fri, 12 Jan 2024 00:42:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7c153a982bfe9879ac96ccc47be6323f83352908f47b0506d64131d93faeef`  
		Last Modified: Fri, 12 Jan 2024 00:49:22 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1` - unknown; unknown

```console
$ docker pull drupal@sha256:59b683bb8204d46558e732d86651830769931f55fdc2362a3212d0f82246070c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b53e5f87ad7fd2718a04cdd085845bc86f53ade17348f77549bdd14b5134fb`

```dockerfile
```

-	Layers:
	-	`sha256:e74e08a81c870e020936e44b8ec63c83a2bf9c828fe421b1fb5d40d629fa3509`  
		Last Modified: Fri, 12 Jan 2024 00:49:22 GMT  
		Size: 5.7 MB (5727634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b132d2176ee556211ab002b5ad65c6d25c4a54f5ef947ca2121da70598c5d1c`  
		Last Modified: Fri, 12 Jan 2024 00:49:22 GMT  
		Size: 27.8 KB (27779 bytes)  
		MIME: application/vnd.in-toto+json
