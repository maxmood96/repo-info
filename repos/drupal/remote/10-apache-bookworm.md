## `drupal:10-apache-bookworm`

```console
$ docker pull drupal@sha256:5c6441359ed725f0132ce0f01bd7d673dd0a3c8f64fdba8879da674e4f6f1ce2
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

### `drupal:10-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:fdbb435f7087e2b35f805b1aebe30560fb36b0d97ae37b5384dec2b4ae2ca47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee76800371e3e13a36ffed02dac81a4a92a65e99fe498a69c9a3697843e2a8d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3257fb24987ade6576f5e97f4099f7708cfe79b4bf5c41a1585248bf31efbb2d`  
		Last Modified: Thu, 25 Sep 2025 21:15:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e065e9a1e2b0e8bfc6cb3f6e8ff75f524a4ddc19d2a58df80e8b6ccf049fe31a`  
		Last Modified: Thu, 25 Sep 2025 21:16:04 GMT  
		Size: 104.3 MB (104330043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb87ef166b76d3ddc2effc87c031ea7153c96d4d282a4e768886a3fbe3fc4e8`  
		Last Modified: Thu, 25 Sep 2025 21:15:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f78c8eb8fc48b30921d518fa3b36283af3762e6548c27b78bd4acd69abe7f21`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 20.1 MB (20131718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36f76d37fca24e7682384bf5e53f187186409122e6d3a6641043619b40a71d0`  
		Last Modified: Thu, 25 Sep 2025 21:15:56 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf735afcf52ab53ca3bbd39c45c1792f4460ef754603c7fc7341861ea8ae52`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2778643c0f7ed9bc34c84c7ee434c9164e9ebcdf22cf49e50e6cdf1b2607d34c`  
		Last Modified: Thu, 25 Sep 2025 21:15:58 GMT  
		Size: 13.8 MB (13774821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae524c29b5f9829a1e92e677636ea528e2dd58cca886ad1b8a8fd4ce2c508e55`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e6ddd8f328f3e21604f1674d4b30b4d8315d19e9eba3ade13ab9b618f2e41`  
		Last Modified: Thu, 25 Sep 2025 21:15:59 GMT  
		Size: 13.5 MB (13496004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec260ca74c764252b0260c2e792a5484e1b0f3fc8ee043e77b6a1541b58bc3b`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af5e09a484e04c2802724538c72cc20829e721928afe30a3a5afc3cea017397`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ebbe56004a3dafceb117f7fe1336a01b48f44421dd37e1df21142df1647e01`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2565d5b0ad48c572c97bbe66d740d06f8d386499c62a7cc7f39c3961faa87b9d`  
		Last Modified: Thu, 25 Sep 2025 21:15:57 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba0516127910d7675e438e402b012dfc61f680024980c54122b6f679e01b318`  
		Last Modified: Thu, 25 Sep 2025 23:16:06 GMT  
		Size: 1.6 MB (1574078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7d5ca31185a05616cd7c033c11d0be57e2d84e266e241332dd9e1945491c9`  
		Last Modified: Thu, 25 Sep 2025 23:16:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b24a7688b4727a75b8693109c92794707c7e522774756fec0182733a260cd17`  
		Last Modified: Thu, 25 Sep 2025 23:16:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19ade8bd252b575a8680385227b1fa66c41f3c03a181dd2311d628dd72e114f`  
		Last Modified: Thu, 25 Sep 2025 23:16:06 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b11fa3c4f3459d60d3247f8c9d3adfe63289d1441c057c0aa2504a1da30cfd8`  
		Last Modified: Thu, 25 Sep 2025 23:16:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc1df9f73fb07f5c00e362805c1634c02eded9a192154ed5b245d5109325a70`  
		Last Modified: Thu, 25 Sep 2025 23:16:07 GMT  
		Size: 21.6 MB (21627375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bf9ae3bd19a8b7e9d8c74dc5366051c1ae55ed5a6eed0018ce55c0510cbc9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7088891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077b9d2eedcdcd8aa1181d084a9dc888a3a45137bbd534a78a49e301c60c6be4`

```dockerfile
```

-	Layers:
	-	`sha256:ca61e5c77fda8207ae39cdcacc46ab0873af760a9cf885ecf0ae19338aaef55b`  
		Last Modified: Fri, 26 Sep 2025 01:54:26 GMT  
		Size: 7.0 MB (7045409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2c1e3354b3fbd2f6c605248d30958d1d08b5d0da099c084365e1bf418519ac`  
		Last Modified: Fri, 26 Sep 2025 01:54:27 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:0380625a03955e009fe897f863e720b699752de9145b7233f2fb0a8ca4ff29b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167994971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf0dc33cea49fcb7efd961b4962099572f61798b46459b47bd3e7d6ada05358`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0026bb14f8dfe0405391889b1c511989ea4ced556f0b3c8adfa59e7529c05891`  
		Last Modified: Thu, 25 Sep 2025 21:23:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e030dc8e3ce0d2390f38b20249ef6ed2b90d270653692a9368430d095133cb5`  
		Last Modified: Thu, 25 Sep 2025 21:24:07 GMT  
		Size: 76.1 MB (76148290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59104aabcb8b8c27fb1c6f04550a2181503e824b232fc921189d4a873b5bc95`  
		Last Modified: Thu, 25 Sep 2025 21:23:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca7326eacb36270c6deb1654a20fa180c43a30156c34553a079a0d2f75f3e7`  
		Last Modified: Thu, 25 Sep 2025 21:24:01 GMT  
		Size: 18.9 MB (18860146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b119afddff180d8cefcaf60751933f658d2f8967058b94b26e72dd96a7cc20c7`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf42dd3adbeff29a4bfb4e982bb9fe44b47b8688548ef6efc28d39ba2b473c`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d4711cce776d37e5bdf98cc079439e681e041be4899f2b92a675547e054a5`  
		Last Modified: Thu, 25 Sep 2025 21:24:01 GMT  
		Size: 13.8 MB (13772780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167ebe197676fec12917f667a8b58c2c00e739c75861cc760c4af9b6ae0c4960`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d50e99f222e23e6ae056c7a044777cb80bbb2beead9ce0f5410aa27f4f75c51`  
		Last Modified: Thu, 25 Sep 2025 21:23:57 GMT  
		Size: 11.6 MB (11599741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07946aed6e5d59ad1ff4d8db027b38ad6128f3a47a3fb33065ea78615bfed1f`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9556a925c7dce21bc591d80591ce991c2146f884fdb80ae3a516d752eebe6155`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1756f27917ad250c1eca56c0223cdc142189b79af8ef5cae2bcf66289e2697`  
		Last Modified: Thu, 25 Sep 2025 21:23:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6168ccd94a953354ff1b062dcc5b19f3b713e4b3ee9fd9b76c9d7f826a558dec`  
		Last Modified: Thu, 25 Sep 2025 21:23:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a4426df4925edf106a5abe64e57975124b8970cc0b88df6ae0eb2216b35045`  
		Last Modified: Thu, 25 Sep 2025 23:20:03 GMT  
		Size: 1.3 MB (1294969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f5fe7c7d86053f61050c54952660ab7132860548e984add7ab93391ccaaa7`  
		Last Modified: Thu, 25 Sep 2025 23:20:03 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca40c2112a06d911c00325c52fd05957aa7d3b9547b148cfad08bf9918480059`  
		Last Modified: Thu, 25 Sep 2025 23:20:03 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2495ab8e18b0fca506d294615bb2258328c9298a3334de60762081270c81bc4`  
		Last Modified: Thu, 25 Sep 2025 23:20:03 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c2a5b7f46fb5554c1e9db3232f574641e01ea48a53a517572b7478eebb638e`  
		Last Modified: Thu, 25 Sep 2025 23:20:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed8be5d9dce6f2b6f68345df6fccb0864cd6c57fb3b0c120c53d1ada7e5613a`  
		Last Modified: Thu, 25 Sep 2025 23:20:05 GMT  
		Size: 21.6 MB (21627250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:07a05df7c2e82e33ae5288e4df8d46e7ba7a4a4744da27d260ba82e8045f9636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6902393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945ecab27a902bc3805c74e172c2646f9abaea66ea81d0e0e7513e5721ff5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:874a207e0c50cc159ec7273dd976cf7cd5c23c385e70d0c665af722bbe74a783`  
		Last Modified: Fri, 26 Sep 2025 01:54:33 GMT  
		Size: 6.9 MB (6858761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bf9b2dd0a4a90be4152309fe6920cab80169e1ba947266b97b0203d9952308`  
		Last Modified: Fri, 26 Sep 2025 01:54:34 GMT  
		Size: 43.6 KB (43632 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:2357421899a1b6093098f5040327fb33ea8af4d348039efe52c976ba31c1f323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197285351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db77cff89e1b5e7d696120628b89e73e10991f4b819c0089ec8a28acc0129f3d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa62a7606711e07dc25db6bd1e7f5ba0ff31ac97d16c04f45b358417aae49d`  
		Last Modified: Thu, 25 Sep 2025 21:16:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534d6e8d75616f3a9d56cd93a6c8b2b3379ff358aff389a7c83e4f6cacd5be1`  
		Last Modified: Thu, 25 Sep 2025 21:16:07 GMT  
		Size: 98.2 MB (98165258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5274e18b0e8ff4cc7764a7dad9c6dcc8d42c3bee294173528f7daebc674f56b6`  
		Last Modified: Thu, 25 Sep 2025 21:16:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5f325939c5b90cb0fba5354346d5b957272f5ae916a464b9774c4eeac309d`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 20.2 MB (20159093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4822a4698c227a70f4168438cfa4dccecbc161d21c43509740cdb3ff1e3a48`  
		Last Modified: Thu, 25 Sep 2025 21:16:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef77a8c3b4970bf0fb9624f65acead93d1e7949b04e013dfb457c19dcd6d811e`  
		Last Modified: Thu, 25 Sep 2025 21:16:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d713c536a71eed6152288198d466cc2f458aeb04d3408f7dfa980c7a0bdcac9`  
		Last Modified: Thu, 25 Sep 2025 21:16:04 GMT  
		Size: 13.8 MB (13774469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a1172dc9a3dc0a9606138b37bea0230fca32556981bdcdad15967d97912c8`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c673ebeef514491f41b34061c6af635954d6cda1df580bc50c0e597fedd5b03`  
		Last Modified: Thu, 25 Sep 2025 21:16:03 GMT  
		Size: 13.1 MB (13139603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e96e32c8055da611323948ca711aa3d5d4096b919cafaf891f5d53fe480549`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3168ee64417fb5d6bf6739e2d0e99b178c270f6a506b1f34c97a414702a0cf0d`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855463ae0db1d1f6b0ea54efb2c13b0c4be438af16e0b44744fe9ca54561d3a`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a44833b35d87eaf1479a091880d518ae938ed7e9838f9745d27a916d0b29f`  
		Last Modified: Thu, 25 Sep 2025 21:16:02 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5bb943d348ad068ded7c04bbb98035a24fabcc434566708148e91f82f09a43`  
		Last Modified: Thu, 25 Sep 2025 23:13:09 GMT  
		Size: 1.6 MB (1559696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9838d2ff6088c2af28b0c78345cbb62aa6f766e44dc6004dd5c2902f886f30`  
		Last Modified: Thu, 25 Sep 2025 23:13:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4beadebd0d4f4e294b8629b11208beda81302388ef57c385389b9b464a5c928`  
		Last Modified: Thu, 25 Sep 2025 23:13:09 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9231a43f6835150c72fa03c74f0455f2e80b8d224563365334ba0ee5dfbb53`  
		Last Modified: Thu, 25 Sep 2025 23:13:09 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4a1952279996204e42bee0eb01c9754a9dd4cda5dc75d1fc815523856da03e`  
		Last Modified: Thu, 25 Sep 2025 23:13:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4bbcdd75ab1c953f78b91f3592d3f8fa491f4d76e75d04baa039c67ad5b1ea`  
		Last Modified: Thu, 25 Sep 2025 23:15:03 GMT  
		Size: 21.6 MB (21627229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9eb9f695013e1edf4e541aa11e303b588093fd79fb4685186559106c5bf77f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7117521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c7562a6e1396d1b12d99297f95440f7c64814bcb5119771e76cf9b53292bb6`

```dockerfile
```

-	Layers:
	-	`sha256:7a0fbce652a02ffba30d2d0d196e2e812d54fb9aac82c73415de3018bcaa5329`  
		Last Modified: Fri, 26 Sep 2025 01:54:40 GMT  
		Size: 7.1 MB (7073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e685e4a9b36ec83f5648c0f357ff2f635ccc6eca81c3ab6e53d17886983ba24`  
		Last Modified: Fri, 26 Sep 2025 01:54:41 GMT  
		Size: 43.7 KB (43675 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:95eb4b54e08130a9a9e65b908ccc8177d3b4a2deaac631827af3f3fa2cd25b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202979736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ea193870aaa77b0b82a4a58432a3cc267e019f4a19e2383fa99698ed3ef8b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81772f3b5a72f216b447c89277a40ca9ed704a1dfa1032c20aa1b3a101838adc`  
		Last Modified: Thu, 25 Sep 2025 21:21:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e859846f90425ec78ab793e9d52fc3fb77a7557cf0850e9c26d306421a18b6`  
		Last Modified: Thu, 25 Sep 2025 23:13:32 GMT  
		Size: 101.5 MB (101517444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09475946cb9e2f2706822effaa2abd1ab3ba7655e445a828046dfd8c5a8c1d17`  
		Last Modified: Thu, 25 Sep 2025 21:21:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe0db76dec5ef1d556642f37ed366b4c3ecec9cd9e02adac3ce8fd564ae7ce0`  
		Last Modified: Thu, 25 Sep 2025 23:13:25 GMT  
		Size: 20.7 MB (20658418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da62e8aca94c6a807dba7eaec2b6fa28aeb3d08651434fe08faed406358445d4`  
		Last Modified: Thu, 25 Sep 2025 21:21:23 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382bd5215f1e6e081e20b795338605db2c07bf1c77f8293bc38572903ab8e8db`  
		Last Modified: Thu, 25 Sep 2025 21:21:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc49f3554ba0f47cf21aea6d8ccca0d3e79a8a9503f99377eeb38c080f8a12bc`  
		Last Modified: Thu, 25 Sep 2025 23:13:24 GMT  
		Size: 13.8 MB (13773807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52fa7b47b6fc873312f21f99bda7f589d4a081ba03ad3352f9f7b04fdaa6e87`  
		Last Modified: Thu, 25 Sep 2025 21:21:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec3f4a325f1d561fbaeaf05d252aa37ddb2759b45373947c7f7c5505bec8b9c`  
		Last Modified: Thu, 25 Sep 2025 23:13:24 GMT  
		Size: 13.8 MB (13789556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9fae299ea836870d34b6d185dc1b496e91a0f3022e47cfb4b9ef9143fee97f`  
		Last Modified: Thu, 25 Sep 2025 21:21:41 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d23b283cdfc3eb4572cd866673917766ead933316f16203cf51d48c416b6011`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3ee867431ff4bdd9daa84f1b6d3845ec3926778e5010fc0c41090462588e63`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231a742bdb21beb61fdc04e2f0fb26fbb272698d5bbb5715ec9e0a5642ac0ed`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf8b37d67bfb4fefdb7b7969e48f88e6f4d62b62ceb48decab9edb1afbaff89`  
		Last Modified: Thu, 25 Sep 2025 23:16:55 GMT  
		Size: 1.6 MB (1645547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b39e9cdbb2887903c3a7ef5ad3837dbb5bedbdd39d6a0b520038139b5d272d`  
		Last Modified: Thu, 25 Sep 2025 23:16:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e210375d959a23f40e9b0455887c315ab1abd63c35d651a9e4f0b9408312c1`  
		Last Modified: Thu, 25 Sep 2025 23:16:55 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceb26a4cbd6801e2f500103e2c73dbf5f283e7aca532df707b4f9e8f5cde4a`  
		Last Modified: Thu, 25 Sep 2025 23:16:56 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5016531c9aaad93c61636f67ebdde3200aba4b5d848d9a94838a237781afb699`  
		Last Modified: Thu, 25 Sep 2025 23:16:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd64dd1b5b88fcacb3aa0e4af66bf9a2306508c9f57a6e4697318c328d8f1a4`  
		Last Modified: Thu, 25 Sep 2025 23:16:57 GMT  
		Size: 21.6 MB (21627420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f83d3c51e696b1a4221c99a00d8a9368ed3f28eb6f9a2492e3c4a3faeeb14a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7068575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be997f9e575105cc3c00b0f7343cf002c4140a5b38bb29276c5351c9aa1a746`

```dockerfile
```

-	Layers:
	-	`sha256:9ac98e49eb8af5a4ef69f96940c8ef1ea8da54bdb56711ff9402409b5ca2f589`  
		Last Modified: Fri, 26 Sep 2025 01:54:47 GMT  
		Size: 7.0 MB (7025147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb321398b5d6e41195d36ada49df6bb5abe07ea98a97bf4786e5effd2caff15`  
		Last Modified: Fri, 26 Sep 2025 01:54:48 GMT  
		Size: 43.4 KB (43428 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:d3260c4a4e24a0f157a0956478a8c077d1224601172d744572a47190f396b010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208565345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b8cffe47438dc16654d37156cd3d9f9411d3cd53029a036d32383d74d135e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b718dfbf30efefabd89a360827a0b382c1a750431b7813dad12100f5b2d957b9`  
		Last Modified: Mon, 08 Sep 2025 22:56:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a384d4bbd9a902a736c45c1f1fb0ab0daaeebaa226229794c25cf0704531f6`  
		Last Modified: Tue, 09 Sep 2025 00:03:56 GMT  
		Size: 103.3 MB (103329767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f6fcbb556c98169c9fadc10cd8cd040ede01c93998afde59bd75b889e7918`  
		Last Modified: Mon, 08 Sep 2025 22:56:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e37b5d8db3766da116967ddda1de068376a26d2ebb0b90928d2f48cc95020bc`  
		Last Modified: Tue, 09 Sep 2025 02:32:11 GMT  
		Size: 21.3 MB (21317791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c89b1d2edebb8bd71e7d951d46a7b39322e076832c5b39c45f8cb6d78f1e68`  
		Last Modified: Mon, 08 Sep 2025 23:25:59 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01e04318bdec0310bba1c446c3523d1f74bc7b2f735315af7604e642c7d7e5`  
		Last Modified: Mon, 08 Sep 2025 23:26:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f0a3d1e3883389eb76974a4a8627e1ff42a7dab8a49fbaa621841cde985b15`  
		Last Modified: Thu, 25 Sep 2025 21:39:06 GMT  
		Size: 13.8 MB (13774237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3e9049d5b842c548dfb445bcec164b0da7481a9c5e428ec3d0476797fdead0`  
		Last Modified: Thu, 25 Sep 2025 21:39:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bca0f51dbf4e50fb805e5175187dd39e355b798fc598def76d09c5c50e3891`  
		Last Modified: Thu, 25 Sep 2025 21:39:06 GMT  
		Size: 13.9 MB (13914308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a4a5633fefa59f11be2cf846027a9c9d97e05d764305aec2d1b330acb47b7`  
		Last Modified: Thu, 25 Sep 2025 21:39:05 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdeb1be4fb5aff6a7590703b32a21a5abff4ed8e2676a66f924eb1e09486348`  
		Last Modified: Thu, 25 Sep 2025 21:39:05 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8728533b4a662f73e1bcb43f7a301103862f15cb3da0bcb7b6aadeae42752244`  
		Last Modified: Thu, 25 Sep 2025 21:39:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69659247b95c4e36b100519bdfa49cee04a9e1cb535fece37348ea99ad52fbba`  
		Last Modified: Thu, 25 Sep 2025 21:39:06 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a339ae5c5608eb99fa807fb72cb1e57d47d43d996db6a71f6fcd026aa94803c`  
		Last Modified: Thu, 25 Sep 2025 23:17:05 GMT  
		Size: 1.8 MB (1775411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a689025391d2fca2f7dcf37d59d401afb68f1681e70a09233702344197e06`  
		Last Modified: Thu, 25 Sep 2025 23:17:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855e9e8cd6e9567e43a4092776873c91a5bdad92524894168689760d44ffce9f`  
		Last Modified: Thu, 25 Sep 2025 23:17:05 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34b09dde3f03c38b01404fbfd11d2b86c8019c633f5be267da20cbf408b7097`  
		Last Modified: Thu, 25 Sep 2025 23:17:07 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3ec3c619c27f88c190b3becc1772af43278ec97aa38821fa2f5cf1e91a3eb`  
		Last Modified: Thu, 25 Sep 2025 23:17:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecf93fa24ae0791d09a703e9163253b112c366d618e24a7c9c5810072a6753d`  
		Last Modified: Thu, 25 Sep 2025 23:43:19 GMT  
		Size: 21.6 MB (21627150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2592f4d7878d6657cae5dd330dfe069d2dd24a7059291e393e39883e7ee0e20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7065812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6678a2547ae2397c307eb65407305386501310d3bdf9b6d81c35bee06c3e74b0`

```dockerfile
```

-	Layers:
	-	`sha256:1898cd2779fa3b805e968e372ee2dd0445c5d4dc0b30f0c6518489c272751ef6`  
		Last Modified: Fri, 26 Sep 2025 01:54:54 GMT  
		Size: 7.0 MB (7022257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81109fe0fb93d5a9532b9aba0d1223f6c9ca1ccc17e3bd5e60b352dd71cbdd63`  
		Last Modified: Fri, 26 Sep 2025 01:54:54 GMT  
		Size: 43.6 KB (43555 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:3ee7554449148aceab6fd740cc4eb7bde768f5829c3409e9160787ddf4e062da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177826375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26cad96e38f495a108fe44d3559a647d9a1d08c4dd32326c5b2817f4a814236`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Sep 2025 15:27:18 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Sep 2025 15:27:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Sep 2025 15:27:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_VERSION=8.4.13
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Sep 2025 15:27:18 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Sep 2025 15:27:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /var/www/html
# Thu, 04 Sep 2025 15:27:18 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Sep 2025 15:27:18 GMT
CMD ["apache2-foreground"]
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV DRUPAL_VERSION=10.5.3
# Thu, 04 Sep 2025 15:27:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Sep 2025 15:27:18 GMT
WORKDIR /opt/drupal
# Thu, 04 Sep 2025 15:27:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Sep 2025 15:27:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df841ff7e505d4fda9d4ca2fc6f43de256e6e7393472b40d28f59ba35a6f7828`  
		Last Modified: Mon, 08 Sep 2025 22:34:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41420ac2c224ed60cf62c3c79b21f8da4561a8bc1714c2f8647a00d8739a416`  
		Last Modified: Mon, 08 Sep 2025 23:32:14 GMT  
		Size: 80.8 MB (80827220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547d32c48b5b5b87d099477f23b84bf04e850397addb4511ee17044c558e341f`  
		Last Modified: Mon, 08 Sep 2025 22:34:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cb0082b75d2959f787293170fb9d7cb18babcf1ad1b7655592229485b734d6`  
		Last Modified: Tue, 09 Sep 2025 02:32:30 GMT  
		Size: 19.9 MB (19909848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97e63e7ffa775f2aeeb6e86f01697ec4f177ed89c5b2f335a1845a1026c465`  
		Last Modified: Mon, 08 Sep 2025 22:52:05 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5585bd36d5e6ccc5efab93a9cf5aad3080b6ea1f4a1527c77dee05004a71c60`  
		Last Modified: Mon, 08 Sep 2025 22:52:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f01f6be2cf1583f1df2b998f8a76cb91507c09347fc1f4f42224a600519117a`  
		Last Modified: Thu, 25 Sep 2025 21:37:00 GMT  
		Size: 13.8 MB (13773213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb702846b5f4ad1146fac881ac5395966a1c0324da970f5edca84a47b0e068aa`  
		Last Modified: Thu, 25 Sep 2025 21:36:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ba4fc7ff62f293cb6305df1e01e6557320ba7a9f26b4777e9d820cd0f93b5c`  
		Last Modified: Thu, 25 Sep 2025 21:37:00 GMT  
		Size: 12.6 MB (12561961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e362efe0b97026404ad8a2c987c112125fcbfe17573577f7bfb9d124b71e5b`  
		Last Modified: Thu, 25 Sep 2025 21:36:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0cd46cbca5f2c657e78bdec80268f15f814b47f8de30e1904968b3247a687`  
		Last Modified: Thu, 25 Sep 2025 21:36:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b916ef6f1d1627917777160ebf322b69a4a80fb5588fb3837dae25a79541217b`  
		Last Modified: Thu, 25 Sep 2025 21:36:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2a72232d081808a2829107e4ec3eda3f094784ab40dd7e34ee7438f83c02b9`  
		Last Modified: Thu, 25 Sep 2025 21:36:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c311221f803ab06a0f17385aeee6cdb71feabc61be1f168b06d537435b7a20`  
		Last Modified: Thu, 25 Sep 2025 23:13:57 GMT  
		Size: 1.5 MB (1484637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afb9c60a4cd61252d0971104f652b19833d58bd1f06135cf917024cb5a69eb4`  
		Last Modified: Thu, 25 Sep 2025 23:13:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52325afefbaac9bda4c33ed9ce81ddc11065e28b07a90a63e3b065c50b075697`  
		Last Modified: Thu, 25 Sep 2025 23:13:57 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9fdc10c77921987d1e3dc40d28fe05054604d302f0882e37688e7d71d77aa6`  
		Last Modified: Thu, 25 Sep 2025 23:13:57 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22329738b5e09ae3cdc4f845190e5e616e4b2ca0b6ef7d9a166fd6a2fedf339c`  
		Last Modified: Thu, 25 Sep 2025 23:13:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6668710912b869e59bc964469856231e6e9d163d0bb593318f4c9fb59cc0ceff`  
		Last Modified: Thu, 25 Sep 2025 23:34:59 GMT  
		Size: 21.6 MB (21627293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:d254d481c16edd2c2ac2b8141ebcf29240ec3d1311403944a98a2b9ce83c7e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c829ac0a57f68a65580c5d6736e51f6012ab6a185c08b48eb00073930da7b6`

```dockerfile
```

-	Layers:
	-	`sha256:1a3a2c23f6a4af23e7fd08c8871d4fbfa2d17c4b0cea3ee09dd0ac779daa1eb9`  
		Last Modified: Fri, 26 Sep 2025 01:55:00 GMT  
		Size: 6.9 MB (6882611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ce19d128c8baac92545fddb4be9309101c7507ef584e64d16107172784b8f6`  
		Last Modified: Fri, 26 Sep 2025 01:55:01 GMT  
		Size: 43.5 KB (43476 bytes)  
		MIME: application/vnd.in-toto+json
