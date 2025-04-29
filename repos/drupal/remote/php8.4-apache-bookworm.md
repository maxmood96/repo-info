## `drupal:php8.4-apache-bookworm`

```console
$ docker pull drupal@sha256:032ff34e24a5d96f2019df91f9750e164e59de4161dd0b9f39335487b8ec2abf
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

### `drupal:php8.4-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:8915c29ca285cefdf5f4a84fc9a882c6bb3504b2564be6a5a05f0517bf769a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203534704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8d9f4360abd5f6cc1ba6cecc46120ab488757b587bf977db3d5210f6cc675f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb967f50b8409d60467f918b8a943ba136b9a18f52af4b24e779f323f2ce0874`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e6c0e2c8504b7cd8795aa52aaefd8b52e8ff0d4141b7b2b926ddd3120103b0`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 104.3 MB (104325739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5501b4271d754eefb4789d18d04e63aac50077636b291ee044ce4039aef2d9b2`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f500554d50ef908252e94b92256e3baf363a205fc0d266f76751e001448099`  
		Last Modified: Mon, 28 Apr 2025 21:49:27 GMT  
		Size: 20.1 MB (20123855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ede6a0aec3e565a1d6d5a7aba8319148feebfe8afdc273336f53c625ca6463`  
		Last Modified: Mon, 28 Apr 2025 21:49:28 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbf5cb71282a1da6ed8137d3c9d4c0312a62ca2b8890ef801321b7cf43cd309`  
		Last Modified: Mon, 28 Apr 2025 21:49:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6cf46cc97355d7f0ec255b6650f12083387ce0b6d703dd93c621250eb10012`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 13.7 MB (13741433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cdb9a1013224a21a13aa6ea6227b702b4cfb77157030d30e76a3d6ba632f9f`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93c6ce5c6b970a9c9084dc1e29d68c4f4ac0da5161154ea97ac4cffde373ef`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 14.2 MB (14166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224dc10e748ec3d954e94c3d97932942cfd9715b52bd70d12b9577f4473c067a`  
		Last Modified: Mon, 28 Apr 2025 21:49:29 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd01d11c1b5b4d5016e99ea1dabcd018e5261c7310a40eca97c35ebf127b927`  
		Last Modified: Mon, 28 Apr 2025 21:49:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771758acf9dc3d3a6f49c6c4b2b452873788e4e3132babe885157f9bd3436579`  
		Last Modified: Mon, 28 Apr 2025 21:49:30 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f810a7ea4fd7afabf4c1f81f26c867f38e7ae0b392b0ecd15e268e4efa732e`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 2.1 MB (2129032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7287b9a95f9d9ab4804149dd8ce58162d2d5cd5e10ff2e0f0869432391f0393c`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf07a74053fa42a15f248be2e891779150e434f87bc3472fe92350e32a67e15`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda52131fcc07dbc67ba03ff37710b37f60b8361924c4b7e1ed0109803a6df36`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4640a85dadac3f779f96234500ea5728aa8ddb2d8e6de42e918bd7ae44143912`  
		Last Modified: Mon, 28 Apr 2025 22:17:17 GMT  
		Size: 20.1 MB (20063971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:882ae4ee4d0af712fee69701b5f9c5ebcfbb8de1820e4886a0aa79e788bcbae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6895882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4220c553faa90db64218db88161c7641062d6c989afbf4584d5c02264da3f6`

```dockerfile
```

-	Layers:
	-	`sha256:fb3961b25317576a9743c303024d8c101257174ce3e58a518c09393141b25bc2`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 6.9 MB (6856693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9a1d33374c5739e8d96bb36ab4dc6475fb16823e2da8343b192d0da0e389e9`  
		Last Modified: Mon, 28 Apr 2025 22:17:16 GMT  
		Size: 39.2 KB (39189 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6d9b584450b3d5040c7c2bf4ba26ee25547c88b55604860c0f0dfa5b867dff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167160696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99a2c86b2dae25d3ff4a3d57092c62554fe06a4e946cf5e3cf0bb63f39e22e8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4b097a6bd1e1c6005148baf6fe5c3fc8f71c3806b0533176b9e71d30fae09`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b59a7abdeed6ca1e9edaa9c4d716d1e51f3acd76ac9b8a9593379251477a15`  
		Last Modified: Tue, 08 Apr 2025 02:06:14 GMT  
		Size: 76.2 MB (76162685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e77faae9141f2a82370cde20bb002409354ce3554b28663322cebbfd4d775`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a46700c4cc8c523fd97c1920eda2a65475e59e5b50da04ec094381646cc4`  
		Last Modified: Tue, 08 Apr 2025 02:10:09 GMT  
		Size: 18.9 MB (18857333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b785355f97ba083df35cb14c0fd6f4ca577253c72f4946c98e2965daf3ec4b6`  
		Last Modified: Tue, 08 Apr 2025 02:10:08 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315b72a13f74b37348b5dc00938e06103a423aa74a44181c5cfb4d60cd94140`  
		Last Modified: Tue, 08 Apr 2025 02:10:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff69cfa2f59638993e5be619846dfb1f3a31fd0c9902f051c90a5004df39add`  
		Last Modified: Fri, 11 Apr 2025 17:09:28 GMT  
		Size: 13.7 MB (13739462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7c2b0a5bb422fa358e6cb860e1b02860629e676381d28e965607a65d59e154`  
		Last Modified: Fri, 11 Apr 2025 17:09:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5278e4b6c1bb8dea9f6ab9cadd9f127d3fb862e5773b48f59a5420edbd3f892a`  
		Last Modified: Fri, 11 Apr 2025 17:09:28 GMT  
		Size: 12.3 MB (12277511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe1313b4e9c07a45f34a6e73852edfa31b21a9ea3269c3529960eebdcdc43ec`  
		Last Modified: Fri, 11 Apr 2025 17:09:27 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38051b6df10ca545a218ff6503f26e3100de10e714e64d4969e991d679a3a8cf`  
		Last Modified: Fri, 11 Apr 2025 17:09:28 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5866f0b5b9d89405e6896ece73c59519843fc5349b81e6e0dcaac0bd815b9a`  
		Last Modified: Fri, 11 Apr 2025 17:09:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3e3a2bc097315797d3cbe9cd48e7c06e4e37921952f9c68752216714a28290`  
		Last Modified: Fri, 11 Apr 2025 20:21:25 GMT  
		Size: 1.4 MB (1365459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a153bd6114026e3c18d642c23ec7ffeba74dbe639def41f5713a83ff813f6d10`  
		Last Modified: Fri, 11 Apr 2025 20:21:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ecbc37abac595a0f2ebc6891aa448fecaef2108a3efdfd3f0f6af3a62a8809`  
		Last Modified: Fri, 11 Apr 2025 20:21:26 GMT  
		Size: 750.6 KB (750620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42cd4ac268ac552c709f51e4e34fc6675d065fa63284f34e1a144077041b8bd`  
		Last Modified: Fri, 11 Apr 2025 20:21:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f4443a3859a237207c060c2f7ab10c9663f406b717079b73e3a83740134ec4`  
		Last Modified: Fri, 11 Apr 2025 20:21:27 GMT  
		Size: 20.1 MB (20063844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ca7e7bb131b8c25c1cf9c104f65b62a5df6df3df616cb1f9c4108bba3ef9f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba1341aef0e8849afb78051b1917f94d27e071ef586450f694d28552e28484f`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9996d9b822e4c396e0def453e4ab50abfdbcd316c64ffcc31f1a65766b6d0`  
		Last Modified: Fri, 11 Apr 2025 20:21:25 GMT  
		Size: 6.7 MB (6671727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b13143be1221705e1d66bd9d192867a63de28a9b2d6d30b179c462e1cde5382`  
		Last Modified: Fri, 11 Apr 2025 20:21:25 GMT  
		Size: 39.4 KB (39371 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:58a77b3755d5f2bd114b9e4ada4edca7197407a79d987ae59d9b58abf25df411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196686966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f945ce8b12f6717307add7b6aaa711631e5b037f6f89805ec4cd9f8c1472bbb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c5f6dffca44b4205f0e945a57290bb8e3e1ae585f26eccc2c9828d7f9ccda`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8e5730fe526cc83387586aee6b7883edb46c1cbf4028dd372d5e9cc4aa7ec`  
		Last Modified: Tue, 08 Apr 2025 02:20:36 GMT  
		Size: 98.1 MB (98130393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28e77e2da9013ba78046a81e9835f08797c66738b7838294afd4c12822ca8c`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08e5d87081c943aebec15603635f044e709767399fb9288a5d353191df808c`  
		Last Modified: Tue, 08 Apr 2025 02:24:16 GMT  
		Size: 20.1 MB (20120982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63fc51568c1c2eac81ae1839660c84517f78b8a9f41fb196501391ccd75a90f`  
		Last Modified: Tue, 08 Apr 2025 02:24:15 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5eba2365fced3eefbecb722f27c4db6bc90624cbba0b3bac5a572af06d125f7`  
		Last Modified: Tue, 08 Apr 2025 02:24:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d36a5d49ca6796e16af100680cf676e1bb7f67db4ada16bd978f4b843eef14`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 13.7 MB (13741147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11247fd6eddf5db192ec01f9d1ec6e6bcf9cdef544bb1e3f1ef030227eb927e`  
		Last Modified: Fri, 11 Apr 2025 17:03:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cc14ed95dd17565af4a70348a87c01b8a0f699833600a7342426a8e5132bd`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 13.8 MB (13780153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab188ccda043d12dab6c6d8523f98c54c6b222ad56c52c72f69b38f4a67ffec2`  
		Last Modified: Fri, 11 Apr 2025 17:03:40 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f639e946b2ae59e70964da9d547ff56f73d165baa161ac5e1bc7492fc5e7c92`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4b3d872c68da64a5c3cf244220dff7e5cc3185aed4b4001e5c4e208f2d4a70`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca64ea402d2ea4e520a5b01e92e8261ff2eaa23ed8c8d2908eb96f1c649c966d`  
		Last Modified: Fri, 11 Apr 2025 20:27:56 GMT  
		Size: 2.0 MB (2027662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6049620dd262ecf5950c911001fe5f29fc67a279d6fe0d37b295fa9bfd1f5ec0`  
		Last Modified: Fri, 11 Apr 2025 20:27:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a3164cee0bd77e0e5eb039706ccc0f06e6021135c36e6eb661f0eeb9c330f3`  
		Last Modified: Fri, 11 Apr 2025 20:27:56 GMT  
		Size: 750.6 KB (750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b417f3f635ee4f930dbc0524ebdf57c25cc556fe21e34898d1090d12b20e8620`  
		Last Modified: Fri, 11 Apr 2025 20:27:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439276991d9d67c40a9dfe28d021957e7cd775f6fba981ee3ef6dbfe51a1c205`  
		Last Modified: Fri, 11 Apr 2025 20:27:57 GMT  
		Size: 20.1 MB (20063771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:73f2488c1be51b390704c813a053cdb43170dcf9d48c7948fc6c4a3f22d76ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6924640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614683802bd7795e2a3f73606e7e65fa02c6708cbdb012a8f4486e609b62cf56`

```dockerfile
```

-	Layers:
	-	`sha256:ddd82074b88d4ea54fd8bc6c43a43e960b2f8151eccf2da17ff2b2ae32f99013`  
		Last Modified: Fri, 11 Apr 2025 20:27:55 GMT  
		Size: 6.9 MB (6885201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943e02b4d89d99db46a99b427b7f2dc8928e0f54852edc3075e70a9cc091728e`  
		Last Modified: Fri, 11 Apr 2025 20:27:55 GMT  
		Size: 39.4 KB (39439 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:5e3427b81ea34a67e86284a2c2e1d819ba9da5cdcdf58a4fff7a665de6bd5ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202598773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0055de8d5040fede1c536cfd8566f2871a39406f1b0bd6e4fae5993030851e46`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a606625d58472aed5c6f6539beda7cbe3a34bbe2c0b386c51c6f2fb4b784b7`  
		Last Modified: Mon, 28 Apr 2025 21:48:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9467d589a5063f0e985decf5ab93d5d37b2eac4f9db606b4c292e9e490c764`  
		Last Modified: Mon, 28 Apr 2025 21:48:43 GMT  
		Size: 101.5 MB (101507736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431a8a7baa4872bd3834f9fd130e737cd3a428af68c8676749bb008395069b9`  
		Last Modified: Mon, 28 Apr 2025 21:48:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0788e484bad25fe8150b55d7382f06c2ea5ba237048bd8954983a650afee2e44`  
		Last Modified: Mon, 28 Apr 2025 21:48:40 GMT  
		Size: 20.6 MB (20638450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741da521020ea8a6c4f5ac36232b08631a75b0ae41c624319bf843563ccff80`  
		Last Modified: Mon, 28 Apr 2025 21:48:40 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c48b50a59a10a7e5cdd9d9ea69baf3aba62025dd4d7f5bd366eb363b2e6adb5`  
		Last Modified: Mon, 28 Apr 2025 21:48:40 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954095dcb07199b44da08c81281d502cb76c951894d381e57c66a05ff68061bb`  
		Last Modified: Mon, 28 Apr 2025 21:48:41 GMT  
		Size: 13.7 MB (13740390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202adcde0b89cedc0835d15eea27d909338bbccd04e1cbf34304e7209c7ba14c`  
		Last Modified: Mon, 28 Apr 2025 21:48:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b38b53056c7f6750b0312ea54893ae3a2ddd155b978bc57d266c36a6fb5775f`  
		Last Modified: Mon, 28 Apr 2025 21:48:42 GMT  
		Size: 14.5 MB (14460779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ebfa5ab588411cfd960ba374e6e4995816ff368674429a596689ba31521638`  
		Last Modified: Mon, 28 Apr 2025 21:48:42 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53a52d9658db199db20b83dfc4fc8a5d8b1db0301a68e5098fb25daa4f4f11d`  
		Last Modified: Mon, 28 Apr 2025 21:48:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e65ad5ad71a5e9f4444101318ddef936941a07038d61e8e5a282ff1c3cf6808`  
		Last Modified: Mon, 28 Apr 2025 21:48:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f233fd051b302d44883c2e299cb26b8f8ba2ad29ce457014a1be1feb89e18f`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 2.2 MB (2220070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f98513ae5a1360d69cb41ed5c808846815bad0b7b591e72e34a94b63da853c3`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62d9ce3403a802681743eb2909a20e8cc2a83d9e3d87be10232678fe5e7cbaa`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba70c3d7483f55689f74dac02415aae6d9d9c733e1d706bd300e078a66c6efb`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e123d0e3dcfc30f63a79a45c8651d2cbf128a967000ed28810de245eab061db0`  
		Last Modified: Mon, 28 Apr 2025 22:16:06 GMT  
		Size: 20.1 MB (20063969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:969f7c1ac8cb7eca805d03b95e5b562bc3e4fc07753cdfb9345e86adbd0a65c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6876028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76017636b7ff116113b999a9c8faa55f2e5988022fbaaa99732c80fc971d0ea3`

```dockerfile
```

-	Layers:
	-	`sha256:c8393556b29a040e2a9e06834864d3d80569d776171c14711e75cd8ff100ab9a`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 6.8 MB (6836924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3864f22eef5c8674d7ff67f4df0afd04857eca10c10d7e38048253df9ac7740`  
		Last Modified: Mon, 28 Apr 2025 22:16:04 GMT  
		Size: 39.1 KB (39104 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:9347e10eca9ff343a67e760c599b09ecc3745968e9e8252ee6087a047a5e5e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207709227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5995f5a8d4d18b292f725c2761b3616d56f32fd178c75a5846a12df9d7d1fe54`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0826c2c78ee871653d0f57d9c44ce65866504115c48a8494edbe4acb9069b52`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18cc47752cabbb3e0f444ea51014859eeb381a04a9b84e453b349ceeecfef1`  
		Last Modified: Mon, 28 Apr 2025 22:29:46 GMT  
		Size: 103.3 MB (103313187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72914eeea8bb18897afc016693b242383396e76406f7363c6ba1a9be152145bc`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487cf685ebb89da437ccca9553974ef5d8fd1546d00a240c39c8980e18a9075`  
		Last Modified: Mon, 28 Apr 2025 22:34:32 GMT  
		Size: 21.3 MB (21308396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0caf01294aac11114b41679b137bbd5379d9aadc22bcd925f84a08bdb6c5c2`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7c93db4f2696ec7aa86f3d1c0a2db0345e19037a7bb07c48cdf34351262d9`  
		Last Modified: Mon, 28 Apr 2025 22:34:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2f2be91b25f43031e7ef80f9eb07888db15e0ade88f733601ce41405414747`  
		Last Modified: Mon, 28 Apr 2025 22:51:16 GMT  
		Size: 13.7 MB (13740911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60e7f40a5c350cabc48554f16d98efb5120807dca3b1157e332b3b60f55525a`  
		Last Modified: Mon, 28 Apr 2025 22:51:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0236e651dabb4bc0635118747319197c0d6fba19a56aac781e15431ad528bc`  
		Last Modified: Mon, 28 Apr 2025 22:51:17 GMT  
		Size: 14.6 MB (14587170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0398d99f568fe8f99724d83532d0b65d2ae6a549cd7b5c38c4ad9ba82ca76ddc`  
		Last Modified: Mon, 28 Apr 2025 22:51:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f073c93cdda875c84e890dfacfd259f48ae4fb167ac0ca73427ea72f2f918ed`  
		Last Modified: Mon, 28 Apr 2025 22:51:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8be654d7106b040f4ec0439b25a51e786654c0614e764599a80e857a74a5dd`  
		Last Modified: Mon, 28 Apr 2025 22:51:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3eef763b7bec995686151f5811a7edc8dee0da0d45f4d1790e9a37563d56b`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 1.9 MB (1871110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89415ca60d1b7fb1734ded866d348d879f7161e4489bc7c909ee088f28c09a52`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da97d68c5375fe30e6c6b153b0c78284084f5af8545bb117c8f954ae12fc1092`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 750.6 KB (750629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6db7f033e7713a52ab3fde490590db87cf2feabf21ae454ec54c8877c49940`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38095aebeac6165c86e4be11589efecf9a163899b502ccb2fa7738b026e85142`  
		Last Modified: Tue, 29 Apr 2025 04:39:46 GMT  
		Size: 20.1 MB (20063477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:da1d3270eb627c39e0eba20df9780a6974abffba26381a56d3d2a7ce2a5900a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6873050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6b363ab49ab6611de45cde419c544a342bcabb55baa20df679b596ed0b2b3c`

```dockerfile
```

-	Layers:
	-	`sha256:ae934c20bf9191f12962d6204fe1e2407199ab83d068497ee9c9a9ccab9646bc`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 6.8 MB (6833755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbb75bd02ad07bce80a2eed5be1f434a9c05af550066a5da4da6cdb8bab7c14`  
		Last Modified: Tue, 29 Apr 2025 04:39:44 GMT  
		Size: 39.3 KB (39295 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:776eb4833e8a802378449e65934d3ea1296e8807150ac97719b40f968cf27fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177263357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5eb3eff9b2344997c73829f0ec30986367fa60acd5bb3e8b818ce021814d8fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 02 Apr 2025 21:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.4.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGWINCH
# Wed, 02 Apr 2025 21:27:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["apache2-foreground"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b23990f9b2f689c0958e401e12177302f3c3909b95265780e0ffa1d83f07b08`  
		Last Modified: Mon, 28 Apr 2025 22:11:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7157d5c3015139f8692f9d1c1ed18e722446a58364395c431f006376ad7d71`  
		Last Modified: Mon, 28 Apr 2025 22:11:19 GMT  
		Size: 80.8 MB (80819034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3c86053dceabe42d2b50d7dce807078de19abd3debede2d77be6e7dfc238f8`  
		Last Modified: Mon, 28 Apr 2025 22:11:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a60222c8bce2f2e1af6ab56f8bc6a567757c6517ff44cc0729c656bd6bb65f`  
		Last Modified: Mon, 28 Apr 2025 22:14:56 GMT  
		Size: 19.9 MB (19895098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a971c2aa2f64e34a6822bbabb57a597bc1ea72e2176c924ab85197de162f790a`  
		Last Modified: Mon, 28 Apr 2025 22:14:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1df01745aaebfe5f89669a535345f32d0a7b7149e54131f0fd4f38c4b4c523c`  
		Last Modified: Mon, 28 Apr 2025 22:14:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c89bcfc17b5b01a5b81807c66308e4ae18b2761ce66c04a5d0f0e41a53dc5b5`  
		Last Modified: Mon, 28 Apr 2025 22:29:08 GMT  
		Size: 13.7 MB (13739911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6307de01bc592376d88ffa27d85a6323f633bb6e63e84f9c9c9373d7179c5a9`  
		Last Modified: Mon, 28 Apr 2025 22:29:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbc22d26ffb3d3301b1a3279298b355b9de80e65d1486d711e48931ccadc4b3`  
		Last Modified: Mon, 28 Apr 2025 22:29:08 GMT  
		Size: 13.5 MB (13539507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f0854bcc0c6e8490c62bab04c67d632fb5c093feea7c1efef12ae1bb5860a`  
		Last Modified: Mon, 28 Apr 2025 22:29:08 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe9ede67243d759445dc5870b66b8e76513c3bb130b619c473ab2247c42a17b`  
		Last Modified: Mon, 28 Apr 2025 22:29:08 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df49a71d51af6070c2aa02acd986eb7953e1495884c30ba306b5b5d8311aa722`  
		Last Modified: Mon, 28 Apr 2025 22:29:09 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40a7f055e12922973bde12e5d4a571bbbdb291ad8a308c36150c9026bed7f0d`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 1.6 MB (1564555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155395d728cf1490914aa19a5653828f63190e9c1d2d1f69bbccdeee07ee8fe6`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c570b669ef7de262d0489358f15ca53624348b9757f4cd9ff682d3735db720`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 750.6 KB (750621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe14a89f0c7b4f2d63d200329b41861ae64927fbfa140d504e0d8f0874676e6`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e01d0dca4815d6e61c22c935c45232cdc170909dc951b3fb78385e8d50dfe0`  
		Last Modified: Tue, 29 Apr 2025 03:01:44 GMT  
		Size: 20.1 MB (20063868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:54fe39201d2ab06d327622638d22ea8fb4a55b8a7e5f714e736513aeae4ef2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6737299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd4f15acf323d8b6a6e3e7353f118e7e1320e2071a8c61cd9695233cd722dd9`

```dockerfile
```

-	Layers:
	-	`sha256:70ce4eb3f05757697bb05036d467780b5ad8469dc722d680b487b77ba7fc8e35`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 6.7 MB (6698117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd4eaf8a8e59af6d60c5b518e27d52676ff41704208155a7d8bf970bafb5e82`  
		Last Modified: Tue, 29 Apr 2025 03:01:43 GMT  
		Size: 39.2 KB (39182 bytes)  
		MIME: application/vnd.in-toto+json
