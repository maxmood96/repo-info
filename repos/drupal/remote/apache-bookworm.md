## `drupal:apache-bookworm`

```console
$ docker pull drupal@sha256:b480a62603269d6c3a8d49de7ce9a92e26a65b190a875ff32bf1e1ed301f9103
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

### `drupal:apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:76d76e5c254b969c426ae48871c3f7711a7e2c66dcddb08a2d6d79b1232e58da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.7 MB (205685065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab47aae6c883d325e39a1178c3340f316712dd24ac5589fef9f1b00064c1d1e0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c577c67954c5df61bca62581bc860a12633f20e73264536d78e4200c5238412`  
		Last Modified: Tue, 30 Sep 2025 00:03:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8207a251c00bda60465ee8f48be1fde99cb73a3f43f7b3fe02dc87abe2f2c8`  
		Last Modified: Tue, 30 Sep 2025 00:03:09 GMT  
		Size: 104.3 MB (104329936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81b9120891258c7e395d271b3b5d15805ae6a007acd9186d53992ea9dd8767b`  
		Last Modified: Tue, 30 Sep 2025 00:03:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3a022299d5e35b573005d9f662e33df08c9c74c9a3c7a596c8a32b05e46ad`  
		Last Modified: Tue, 30 Sep 2025 00:03:05 GMT  
		Size: 20.1 MB (20131749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcd4fc56b1766189a8b545d4b4cff5579dc33f9ee6d06a5ec3a398d126e227d`  
		Last Modified: Tue, 30 Sep 2025 00:03:04 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e666f6182b5af7770d3302e9d4dce7beb4472a1ddfc6f91dac0086c0b74d37a`  
		Last Modified: Tue, 30 Sep 2025 00:03:04 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8365dc659272e10de24e65a8c0330ab88f705625b66fca6ce3d2c8fe45b4ace`  
		Last Modified: Tue, 30 Sep 2025 00:03:06 GMT  
		Size: 13.8 MB (13774793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55254b15a878a903e6668bc5b336565c5b153efb4bbb80635d329f584e68b0a7`  
		Last Modified: Tue, 30 Sep 2025 00:03:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35f5bc3873b68c0f65caf6db5bcd20879f971e710d277ab9b437b08ac4b3be`  
		Last Modified: Tue, 30 Sep 2025 00:03:05 GMT  
		Size: 13.5 MB (13496001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623580108d606615dacd8b3d8cc665789fae1f48ab941f4220119f8344ced06c`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aaf45dc01d50263a0de44e4734d00c7a9cbd86a92680204ca932ff4f3b7fe6`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a15ba795299a16500010ac5a9cde013094b9d77b43687da40bcbbdebcf9fb0`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807ad59099e38ed350730f59e6cb4f040cd76d08302c966a9ce5a3a41daeac2c`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b9dc887e0aa18017d3819d05d18ff3ecaa55f41317d7a8f48fed57044aa428`  
		Last Modified: Thu, 09 Oct 2025 07:52:38 GMT  
		Size: 4.3 MB (4327130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574e7e8f7c7a903b37415a50071ba81bff3e9051318726e6edea32e7a690f990`  
		Last Modified: Thu, 09 Oct 2025 00:54:27 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a54d887b52c03d2e13c3c0c91f9ca1c03d46d31ddecd38645682f036ea9515`  
		Last Modified: Thu, 09 Oct 2025 00:54:26 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb70ae73ef7cda7511ddfd4f58a149b86f032f58bfacd9a19cbe3c284abb90b`  
		Last Modified: Thu, 09 Oct 2025 00:54:37 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e213c998ef775f1374127e9bb96a796413253bc47b432a86154c54408b64d886`  
		Last Modified: Thu, 09 Oct 2025 00:54:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffeab94da782a19c3fa16198c85edfa8b524473ea726bf03a11756475790dcd`  
		Last Modified: Thu, 09 Oct 2025 07:52:40 GMT  
		Size: 20.6 MB (20639238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ad228203f0f8c8f0b28f53f2ff81efa8d39f409cac83c76b78b63cd6e954d65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7098350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91e5642349b91096b2a478da9a0809e5a69a447196dfeeb38648afc08fa293b`

```dockerfile
```

-	Layers:
	-	`sha256:35e8cd05eca766654c08658773629423c72058c8b752797681574670f8802f71`  
		Last Modified: Thu, 09 Oct 2025 02:09:04 GMT  
		Size: 7.1 MB (7054222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0020e3ddc131cbb0f837ccf34149fec30327e086d881b604f770a49fb43886d`  
		Last Modified: Thu, 09 Oct 2025 02:09:05 GMT  
		Size: 44.1 KB (44128 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ada11b268c3020c1e65b9817a372021b820637624b77b23088b22aa27e543bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167005414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01ccb48c25127e415cc4ffaef7249552cd0b6742b9de9fde8c3512f8eddfe8f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2765cd81ef3fdcf68995b4d50b9f6538c5b10b81de8c24f26de4f0f5a8894`  
		Last Modified: Tue, 21 Oct 2025 01:29:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4087c6ef5ed2c5dbd0093dd8a41c9abe170dad28f8ac8476f5ecfd1c4c8e6658`  
		Last Modified: Tue, 21 Oct 2025 01:29:32 GMT  
		Size: 76.1 MB (76147418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a8baa3182bfa7f41a541bba1f99b91eab45b9ad138cfa20d47411f68ab8ca2`  
		Last Modified: Tue, 21 Oct 2025 01:29:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633a2c6fd1e1654181730317c578c9bb1d7b0af8be9d3bab618d974046c75ef`  
		Last Modified: Tue, 21 Oct 2025 01:40:55 GMT  
		Size: 18.9 MB (18860083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714b5e5fbdfc2cf01c312c095e0773876704d2ec2fdadab2b1f28469ae0001a`  
		Last Modified: Tue, 21 Oct 2025 01:40:50 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db965a34f77e7716b9bf3de935c34ae0c258f34cdbed6668e3dd6edeffae3226`  
		Last Modified: Tue, 21 Oct 2025 01:40:51 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d49f2af7771aa8199bf192f5ffb5e740b5b22df99f78d8a1ebb1e876aecf559`  
		Last Modified: Tue, 21 Oct 2025 01:40:55 GMT  
		Size: 13.8 MB (13772789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c72e520068dc3e3eab9df2242539d4085c4734e6c8273af1d4e48c012c4c077`  
		Last Modified: Tue, 21 Oct 2025 01:40:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0fc2633dd54c7ae821d678a7d66ff39ba590effaec15621e2a570eff348a2b`  
		Last Modified: Tue, 21 Oct 2025 01:40:56 GMT  
		Size: 11.6 MB (11599775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f51df4d755c02df9e2179c7d71c530ca620ba655a7ece6c6ee6cb2eae1a995`  
		Last Modified: Tue, 21 Oct 2025 01:40:53 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd5c02516e47898cd79d3aac3435a2d937eb24263311d18ec48254c710be00`  
		Last Modified: Tue, 21 Oct 2025 01:40:54 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bbf4f841026997b0c9039d6e6883ca9dfc077ef66c2f95ec9df339ce859151`  
		Last Modified: Tue, 21 Oct 2025 01:40:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ecc4e852aaa3f7cb8ca2a92a2d8f590d04c985adb5eea18a3ae0255cfe9d22`  
		Last Modified: Tue, 21 Oct 2025 01:40:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a883c113eca097120524a3aab751591735c061a28bfa867fe06d90614eb857bf`  
		Last Modified: Tue, 21 Oct 2025 04:12:15 GMT  
		Size: 1.3 MB (1294970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f45a1d8be61e0afe0989d3fdec6c0a1b55b93e4b0cf4a1dfb017eb7d4a7121`  
		Last Modified: Tue, 21 Oct 2025 04:12:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc68004c38e943ad340b5717f9caaf2236269cf03d8250db4351b3b0e84c0`  
		Last Modified: Tue, 21 Oct 2025 04:12:14 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcbb0172307b2031e5611363f16d3d4d5e6bcaff72214a4029063c71d20f653`  
		Last Modified: Tue, 21 Oct 2025 04:12:14 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3746adcdf37e8ddc4e2cf7bcd7b643a3297b5b867a9aadd4b0e4e61187555d3`  
		Last Modified: Tue, 21 Oct 2025 04:12:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a91d56d4ae3549ed0d99c1571ac2c7a9cc0ef36e80d06a3f2a93f82efbf75b`  
		Last Modified: Tue, 21 Oct 2025 04:12:16 GMT  
		Size: 20.6 MB (20638445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:d720b491caffca484d0731a66cb3a4e1c961a2637b418c8e9bd7929f4ecb2c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6911885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb157b74ff49a2a1e542a8591fe34d96372859d6814d930145683659283532ed`

```dockerfile
```

-	Layers:
	-	`sha256:d24f456b9746a5a0842d1c2b87980e006111f4794fe0556566ed9006f97be5d1`  
		Last Modified: Tue, 21 Oct 2025 08:02:02 GMT  
		Size: 6.9 MB (6867590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4371ca349260502684c52b6c3222192efd0c0f5a6129e9d7ee92e8d84f159813`  
		Last Modified: Tue, 21 Oct 2025 08:02:03 GMT  
		Size: 44.3 KB (44295 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:940902d42d21bf8869118db55d32e0efd36412e47b54f01c2ff8bdf4ed23ce5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198884529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654fe4df3971404507296a81a3896bb799aa5eaa9d570a59dc835594c272ff58`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80721381b6be3f8cf4eb1bf88eee7c906d2c4801b666437df512d70357281049`  
		Last Modified: Tue, 30 Sep 2025 00:04:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cf7572b66c2912852e0f43b3760aba18446d3f32ed39b8eed79f81bfd1c316`  
		Last Modified: Tue, 30 Sep 2025 00:04:12 GMT  
		Size: 98.2 MB (98165071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd34021b8177620f4b093ebbe63e5a20daa49055b7d88bf054d1cee0ff61593e`  
		Last Modified: Tue, 30 Sep 2025 00:04:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40212c508ecbc2c78169cd42e0e884fcbeaab3d9dba029f7824c79e117f2085c`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 20.2 MB (20159015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6179e69543df914c83cfc166fd460b525a95e0db2d42370524f0088eab300b0a`  
		Last Modified: Tue, 30 Sep 2025 00:04:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e637a23d8a523df9bdc19c5e9bc9286ea4973d2e886e403228d59a657300c65`  
		Last Modified: Tue, 30 Sep 2025 00:04:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc65e0255940bb82ccc6f086d257cd7440f2c204a691e4a43cf525de4df1506`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 13.8 MB (13774429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c7304bbff777051258836bab09d8092eeb1cf1e34ddf7a05ae29d5632080ec`  
		Last Modified: Tue, 30 Sep 2025 00:04:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67815529dac9c338f513672e8340d479d5f2c259fdc7c4cb228f834eb3883d9d`  
		Last Modified: Tue, 30 Sep 2025 00:04:08 GMT  
		Size: 13.1 MB (13139558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b33364247a707578f01e2ad3da46cfe300767bd99861929cd1770071dd6e36`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818b3e7dc076d9477ead18b467e7c6ef545eab2aa2e50e7ac6bc65fa04fb340b`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b768c6b427402515f21bafd268c5177761918fb2867469b1065176f91e46df`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4442f4adc9809c210c2a649cd208b3c41d442e06d1f591a25979dcc5082c723`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc842d8ac7623ac465bf9d40cc6badc7bc3d0c7411660df8709f62eaea258b90`  
		Last Modified: Wed, 08 Oct 2025 23:24:06 GMT  
		Size: 4.1 MB (4147737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7557f080fb46540752d37eebf2efbb8d604243d51ffb79b91eeb6a37f0a960e8`  
		Last Modified: Wed, 08 Oct 2025 23:24:06 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6311f4858fef3fc7314ea66db7f383eecf3f62ff9600570128fdb1593cc380`  
		Last Modified: Wed, 08 Oct 2025 23:24:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76e3ffcd5c6ec4fa214b16e2bf10c672804303415f4b342063d4930f03c3a07`  
		Last Modified: Wed, 08 Oct 2025 23:24:06 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570620538ce23d11a717d3409bca12a77d27a22d0431eb2df08a5e359c30ac99`  
		Last Modified: Thu, 09 Oct 2025 00:00:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0026a8f290d64086c09f8faab6370b74e91ce93cd74b57d9897f87d87808b5`  
		Last Modified: Wed, 08 Oct 2025 23:24:13 GMT  
		Size: 20.6 MB (20638694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6d3775e95cecadb08f9565de21cfb3dad8212a5de615f124a64d7ea281bdbb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7127027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeb0b7e59cbc14d7f363da386e36d4d5abd7dce06960748fa052709f08a25e9`

```dockerfile
```

-	Layers:
	-	`sha256:aaeb977d9d5422a7d8f9a88007cbe0c6e8fb0cdb15e2d50d83da65e22e1a8940`  
		Last Modified: Thu, 09 Oct 2025 02:09:18 GMT  
		Size: 7.1 MB (7082683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e94884e3dfc20307b663708d93ae2393f8b9b84fa1eaa3bfbeb5b7e08c285f5`  
		Last Modified: Thu, 09 Oct 2025 02:09:20 GMT  
		Size: 44.3 KB (44344 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:193b02019513e77e1d7206576d5ff5f549a0557250ced4b0e1b92a53e0a3a926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204750026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e517793ac335a117ca35ff08b8a337f2e5957d2f6e8d8159ab2f0be9156747`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d3926111a71dbd6617052c68cbaa88d8e24be48d3e9fe293319bbb0d4c47c0`  
		Last Modified: Mon, 29 Sep 2025 23:54:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f2c7184c86b1ba8ab084d35922dfd570f806186509743d52c0f1f49689d994`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 101.5 MB (101517400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b97e3b658156f6504ebca9f7c9b0078c456a9224bca4294eca51f536f07596f`  
		Last Modified: Mon, 29 Sep 2025 23:54:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e9417156aca83f3c4ce32be98f5e5e83977d28970f54ae07ce40b51bc399d0`  
		Last Modified: Tue, 30 Sep 2025 00:02:31 GMT  
		Size: 20.7 MB (20658408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ae482b30ef766908a866e7064cb60255edf5afb58da5733eaef9b3cc1f6fc6`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8cdb229b8015595a77af6daaf62ed1867cc014a77906b7d35f01f90cab95e`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e37638abb135c42e42b12e4a9f4fe3c2e0e8a0939439f46e173d1c63a33ec23`  
		Last Modified: Tue, 30 Sep 2025 00:02:25 GMT  
		Size: 13.8 MB (13773846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386aa897485f927d0bc153e55068367074f9560cbed233c62fdab0929b9523c`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853860eed3387e3451872e31af483cf135ef44d05adf8eb5acd957c3e5559fd2`  
		Last Modified: Tue, 30 Sep 2025 00:02:25 GMT  
		Size: 13.8 MB (13789540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047d1bae1a3266e731502b1159a98decadced2c6ee46665864fdd09a84c8ed13`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455bb28a9707d8f87b2a002d41cba47b9741ff3854c8633498713243eeac5a45`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73281cba0a89d965f03fd76b0382286093c44927f894a564e3fdf41eab4fcf4a`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d1ac1f4a2880538c570d87cc15915e4cfb41438ab1d770bc22a1265884500`  
		Last Modified: Tue, 30 Sep 2025 00:02:24 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb549c3bab4d2b014ea5bf4e331875dfd23adb32855c25f71dac30caa7e3226`  
		Last Modified: Wed, 08 Oct 2025 23:17:40 GMT  
		Size: 4.4 MB (4403938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66407a92eb4bdcc7a3b1571122524f6ddafd74e654145ac24c46f8ef5ef32615`  
		Last Modified: Wed, 08 Oct 2025 23:54:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdf587b16e777397c70a30ea470dfc796a63278cd59414a97ae55b9078a75af`  
		Last Modified: Wed, 08 Oct 2025 23:54:19 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3bac480ef2c72951d93f5601e6eb8aaeeecf7079cddd8703f23635dfdbfe16`  
		Last Modified: Wed, 08 Oct 2025 23:54:18 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180120770bc0041cea4416e7e41394857c635e58e8fe4ad80667aeba1e1ebe0a`  
		Last Modified: Wed, 08 Oct 2025 23:54:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5337b5b568ec5ab69fa6fefa37b7ea56a0c8bc088b7bc385d82249dc71534a50`  
		Last Modified: Wed, 08 Oct 2025 23:17:41 GMT  
		Size: 20.6 MB (20639374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:1f48460b99d5a16592801e69d3f46ff1792f4cf50ab6c87162b8d67bd2877552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7078013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8cb70324f980807f3fa5f66afb34df440212435858894bb566b0a4889ce170`

```dockerfile
```

-	Layers:
	-	`sha256:c980320501dddc7bbed7101cfb53e5c60a62f6093bb271e65c1d064999d76dfe`  
		Last Modified: Thu, 09 Oct 2025 02:09:26 GMT  
		Size: 7.0 MB (7033950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107c57f014f45df1bc9e1adfaa9e6cc64cef133332617c60a89bd7cf83c0337e`  
		Last Modified: Thu, 09 Oct 2025 02:09:26 GMT  
		Size: 44.1 KB (44063 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:e412c0b15d3ed45ee225577c13b1ced502314c4ce62de0ad28dd07018c41b9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210534465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54cfe079fcf57985d452b83eb4d8b86cd63857beffebe12d4ecfe9574919ffa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9224126999b17ea18ad3192bf1f731d4bb9aa32a52f09c442a3de3ba3b786f3`  
		Last Modified: Tue, 30 Sep 2025 00:21:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e6783fc03077e22b7c9e12c11882548b0054a2663a8ef49358f7327baf349e`  
		Last Modified: Tue, 30 Sep 2025 00:21:18 GMT  
		Size: 103.3 MB (103328743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ae54ede2b3ffe909b51995334afb653bfac09e40805963f18c29327385318`  
		Last Modified: Tue, 30 Sep 2025 00:21:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e826edd8f76372320eb04b480569c9550cc354df72e5453efc1e24f8ca6435`  
		Last Modified: Tue, 30 Sep 2025 00:26:39 GMT  
		Size: 21.3 MB (21317847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eacfec890bc561637d332e33d282a65c2cee7448068ffa32b8bd41b9d125d2`  
		Last Modified: Tue, 30 Sep 2025 00:26:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a5094e1ce142c1a5814e699f6a3866a8717dbe8a8afb25a8345bb4dabf2de6`  
		Last Modified: Tue, 30 Sep 2025 00:26:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b72622d731a18885418a8a4978356a4d106d4a868291e2e9aedc14a59cce37`  
		Last Modified: Tue, 30 Sep 2025 00:45:37 GMT  
		Size: 13.8 MB (13774242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9949b191ce6a304e5e479c7856c3b8c01c37f8fc5d65bb60fd71c15ae43e445`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad707eaf0523cb842cf264a73b3584e029305965fdc6338ddedd15d87b4a3cf1`  
		Last Modified: Tue, 30 Sep 2025 00:45:34 GMT  
		Size: 13.9 MB (13914342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79465bd12bcd7f02c45bb9073929f5975444953da30133288d2375b303f90db8`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee584c9d6fcdcbaaacd3626771f3cf2cdfa2fc23589acd99c97e552bf46b786`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4168ba5653914f32e80e6f9c301fc0e4809c4c9bdc4f66e927feb7dfdc5ba2d`  
		Last Modified: Tue, 30 Sep 2025 00:45:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af720b2ecf074e65bb133449e00031abce7b9b5aa5ed916ff16ecc055be7951`  
		Last Modified: Tue, 30 Sep 2025 00:45:33 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77574cb6336b7e5fa378c5f36d7e535a141d1059dbc6c2c8cdc4c4ef18301a2`  
		Last Modified: Thu, 09 Oct 2025 10:17:23 GMT  
		Size: 4.7 MB (4733479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af1aee3f9ddb73a55e3c163c3f61275ecedf8cbeb1953c1470e037d0fc94c69`  
		Last Modified: Thu, 09 Oct 2025 10:17:23 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddda3b94be20c6b26d89a0f415701ec80e7be38cca3fd4af19eb1ed8f9e2fa8`  
		Last Modified: Thu, 09 Oct 2025 10:17:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ad325f9b8fca2199aa39a7d2b98f5b17c6db0e8795155ce6a8e80df118cf9`  
		Last Modified: Thu, 09 Oct 2025 10:17:23 GMT  
		Size: 751.5 KB (751479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031c125dd3b7715173eb440a90068e3a5ffb72eef95c563a9b7ae7d77728555`  
		Last Modified: Thu, 09 Oct 2025 10:17:23 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f6b6abe7ab201dcb257d41aaf40343dce03e9b7f00acd829e8357a7e4cf651`  
		Last Modified: Thu, 09 Oct 2025 10:17:24 GMT  
		Size: 20.6 MB (20639221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6a0635e6ed54df65f7347350fffc41049c05ec4e5c65332d20edfd3de0010052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4029b0ec2c59f015359340fa04288f0a23a58737910e9ee1630392a181b9d189`

```dockerfile
```

-	Layers:
	-	`sha256:9e4ee859b8ed91c5bd0824876af424142fdcacdc7b23bf666493ba473c6ed783`  
		Last Modified: Thu, 09 Oct 2025 14:05:17 GMT  
		Size: 7.0 MB (7031082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f43bd6d5ab4e065a61265bff58ccbf1bf45256ff8b16b92e99e96d9539feb25`  
		Last Modified: Thu, 09 Oct 2025 14:05:18 GMT  
		Size: 44.2 KB (44212 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:05971853e769339d6f82c03e7b0d407da472a122a988ed3d253d38b3c811e2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179257455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb7e7487c8d5d62a7605d45bd57e3949aa4441d07d517a895447388a7af77cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
CMD ["apache2-foreground"]
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV DRUPAL_VERSION=11.2.5
# Thu, 02 Oct 2025 09:46:10 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 02 Oct 2025 09:46:10 GMT
WORKDIR /opt/drupal
# Thu, 02 Oct 2025 09:46:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 02 Oct 2025 09:46:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d82124f58a645a9da3f15f3da28d4ca1455d28e5d91846444d1052535447d`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b01b9ac7d1cffa33f9a421d32a8141448890b76a8a421333ce992c42c236f2`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 80.8 MB (80826420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f8a2c56e71c89a84dc64f20767ac8e393ae6bf31491b671931026500a94fa`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3685d083390bd60c92d11c2e2ab236933b2524cd63c252f67bc317596f4e4b`  
		Last Modified: Tue, 30 Sep 2025 00:08:30 GMT  
		Size: 19.9 MB (19910066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a5638c8e94672d92902c3cf9c6c0393af360f85f2aeacb8367aafe726448bc`  
		Last Modified: Tue, 30 Sep 2025 00:08:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf8ee6849a38404ca53b58991fcde9db799e42b9656d3c6688293143ac44192`  
		Last Modified: Tue, 30 Sep 2025 00:08:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb221426498bc7201d533cbb5d495b54d7c6628ed0088df7b250f85c70da22`  
		Last Modified: Tue, 30 Sep 2025 00:24:08 GMT  
		Size: 13.8 MB (13773186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca2ee2f83511c4e21631f3ba42d23eccc3290afe448ba0c59b29a2fd9093f40`  
		Last Modified: Tue, 30 Sep 2025 00:24:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940c1f9e8a0cea995eb66bb2387e9d9c2e29bb9e800149eb640b53f2ca0cb6cf`  
		Last Modified: Tue, 30 Sep 2025 00:24:10 GMT  
		Size: 12.6 MB (12561919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66eacb389bee1c7580ef659c9b1fc7486f6fea073018fbb9d56a6b8a851c6635`  
		Last Modified: Tue, 30 Sep 2025 00:24:10 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63e758bc5ba1d667c9816f274285407a8fda67cb1d71db43868d22aaa725af9`  
		Last Modified: Tue, 30 Sep 2025 00:24:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58d7fe768e61f19892e6312bbc2fc6e0fc74c0346075bbf0a4e4dbfaa83ee2a`  
		Last Modified: Tue, 30 Sep 2025 00:24:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51114b41b44566b85606a3701a020080f6fa33fcd771163335a18ea53398c588`  
		Last Modified: Tue, 30 Sep 2025 00:24:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405d7f54a67eb4e90c4fc28a72b2a69f7017ebbab71f055a473e862c848c8fbc`  
		Last Modified: Thu, 09 Oct 2025 14:43:02 GMT  
		Size: 3.9 MB (3905668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6750c9fe6b77c91fc67d7f80af4ffcec7e04fb6469e044dcbd7cf3378e97d7`  
		Last Modified: Thu, 09 Oct 2025 14:43:01 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3de2c455da2f5d908c275411f5e2a52e374fdb5fda0c44242e1a990fbdab5c6`  
		Last Modified: Thu, 09 Oct 2025 14:43:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15407241494922822d4c440680f8bbea3d55306efb22abe102c422780e52db`  
		Last Modified: Thu, 09 Oct 2025 14:43:01 GMT  
		Size: 751.5 KB (751480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa253edfc50927cec4e1050479664a88bee273dc6c2f85edcc35d873e4f2b1c7`  
		Last Modified: Thu, 09 Oct 2025 14:43:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab869bafd1d55cdd8d2a76732d5db44441dd0591da9c1b4f90a3264d6c33b9`  
		Last Modified: Thu, 09 Oct 2025 14:43:19 GMT  
		Size: 20.6 MB (20637983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:75aa126d9c693eeaccc60d8bd8603e1c4b4f1c7cc9b4ad7ec6081776c607f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f67b441fddba284ba79d09171371f549c873d8818b6b67f43a2a07b1636942c`

```dockerfile
```

-	Layers:
	-	`sha256:ebde7f613b95e406e32faadde0070721806f005f48f5128975b6fd2b7b3d7d1b`  
		Last Modified: Thu, 09 Oct 2025 17:03:40 GMT  
		Size: 6.9 MB (6891424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0fdaa8eea798ff80020b7be2978caa35d0be4db10eaf23400cc9d99f6770265`  
		Last Modified: Thu, 09 Oct 2025 17:03:41 GMT  
		Size: 44.1 KB (44121 bytes)  
		MIME: application/vnd.in-toto+json
