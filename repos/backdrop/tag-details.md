<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.30`](#backdrop130)
-	[`backdrop:1.30-apache`](#backdrop130-apache)
-	[`backdrop:1.30-fpm`](#backdrop130-fpm)
-	[`backdrop:1.30.1`](#backdrop1301)
-	[`backdrop:1.30.1-apache`](#backdrop1301-apache)
-	[`backdrop:1.30.1-fpm`](#backdrop1301-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:4be888f1c3dc7f12ec8127f2b999ee765f97cb4469b115cfb247e42598c286a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:b50428e2fd1b36cf43346258044e9c25be4fd62fd12244e95e493d4272e2fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187429753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650c622d5d1939636f59556367bb745ea4efcf0cb628481ce7ed47fc1b5c12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c13e0a380d1066144c01cfba2ab859d271383069f8c2b442f6141a93b518`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59086e1f0cf9b61be62079647cdc4eb36b89cea5edff168417222bb22b103614`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 104.3 MB (104329136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf44beef353412043b2b3904037068ca43282275644dc9b25bab39318df2e2f`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6f0658675ec128165643f91dc72a063ebc6ddff00c2fa1a0a30e21bceafa9`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 12.7 MB (12670866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c52b4d55386b4eb029ceb7084de7fd0755bb27068f7e5386d09191500cf532`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd31f0048a04f2deacdfa04e90000a90da078da75b8b711b6c82eef396b3934`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 27.8 MB (27828243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e79a7d807db4cf18efb8c69c13baefe71d1794e42bad07fa2f1d5d4e27b867`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789f3e28059cc460aa7b42e702b9031ae9a8be7a6c5f9a1cdef49b8fcfa5edbc`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79abfc0ffe8fae80874cefe1dc5a68e73f7d831fb061e7f0adc8e6c0729c376`  
		Last Modified: Mon, 17 Mar 2025 23:18:10 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a50659b9d6949bd73a7423e49d53e7615839c6090753685671927d4ad2737`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 5.6 MB (5588002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af74eb1ddb5c4f4102c3401b1979197f8c3ae0cbadbcfa3e7088be7257982`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 8.8 MB (8794824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b96a5d219cafc293b68f995eea0528b3369efd25a46e311d24555ce8af1c1`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ce7da6f5dbee9cccee7a374cef703a1f6d58e7c6ceb44277befeb7b342f0ba7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dacadaa8e05016a6b0fa31f1eb111451d528b113d2048ba7506c60117c8f576`

```dockerfile
```

-	Layers:
	-	`sha256:41bb2cc6c12011a90b448e68cdab8cd47650effb3b281a708bb90450d2bd2045`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 6.4 MB (6429804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521730d2f4f9a7008aca3edcf3cbd555ea40389be2b67f105dfab454cc1cc16`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3d454b9bb282fc4b224560916df60eccaebb709ec5c12d51636cf2e0f0f269fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d72e237511d698382d62204c8899137f9dc69cbf0d44e74997414f8b3098`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19612df6c8b11eab84a5bb5b44627e00dda3eb5c29a447f494160d040a65be`  
		Last Modified: Fri, 14 Mar 2025 02:35:35 GMT  
		Size: 12.7 MB (12670786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e86b8a62be947487f7600d97973fd3bec39aa741065ac318f924584c42f4fa`  
		Last Modified: Fri, 14 Mar 2025 02:35:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd5ed02f9eea3f69b028908cc3bb42a7802cbfcb9e7c4b650706fd5e00eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 27.8 MB (27772449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d59bb902b97b58e0ca6f094a7cded9325884cdc29dd3cd8ec38cf7a5381eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1b487ac17f877a44f7dd3f30e241e0823150253e7a38f462acaf8ef2112c5`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98067ac8cbae75bbf2f044327990c759767da17c105c01cfb95c3374ee99e453`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14531b3ef2cef9e184f53e2b7e4e7c9e8248ca64ece49f4fd54af8a0f223d07f`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 5.6 MB (5601721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b906ba031f251bf0ef0a242f4e60886a554e681d095c997810f7435e91cf8`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 8.8 MB (8794808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c8576bf52489b87209e8f870c9359d00a83dbf0e12cdbbfe63c8553cb1d3`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:359a6d0257f11f723c53d31702f41c9b18f79212f4170a16c0a6c41bde36ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c7f595224b74c8817efa0a8c1b10c0f457dcce703e928cbe73604961603b3`

```dockerfile
```

-	Layers:
	-	`sha256:7f9e77adf90b5eb89666b262a468cb6059d123e31bd2659de464d7b6b6809161`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5334c6c7f7762ea59823ab0c8ff88b62b37a0760af0c6edc25aeb90d8d6c59`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30-apache`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30-fpm`

```console
$ docker pull backdrop@sha256:4be888f1c3dc7f12ec8127f2b999ee765f97cb4469b115cfb247e42598c286a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:b50428e2fd1b36cf43346258044e9c25be4fd62fd12244e95e493d4272e2fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187429753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650c622d5d1939636f59556367bb745ea4efcf0cb628481ce7ed47fc1b5c12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c13e0a380d1066144c01cfba2ab859d271383069f8c2b442f6141a93b518`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59086e1f0cf9b61be62079647cdc4eb36b89cea5edff168417222bb22b103614`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 104.3 MB (104329136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf44beef353412043b2b3904037068ca43282275644dc9b25bab39318df2e2f`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6f0658675ec128165643f91dc72a063ebc6ddff00c2fa1a0a30e21bceafa9`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 12.7 MB (12670866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c52b4d55386b4eb029ceb7084de7fd0755bb27068f7e5386d09191500cf532`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd31f0048a04f2deacdfa04e90000a90da078da75b8b711b6c82eef396b3934`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 27.8 MB (27828243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e79a7d807db4cf18efb8c69c13baefe71d1794e42bad07fa2f1d5d4e27b867`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789f3e28059cc460aa7b42e702b9031ae9a8be7a6c5f9a1cdef49b8fcfa5edbc`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79abfc0ffe8fae80874cefe1dc5a68e73f7d831fb061e7f0adc8e6c0729c376`  
		Last Modified: Mon, 17 Mar 2025 23:18:10 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a50659b9d6949bd73a7423e49d53e7615839c6090753685671927d4ad2737`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 5.6 MB (5588002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af74eb1ddb5c4f4102c3401b1979197f8c3ae0cbadbcfa3e7088be7257982`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 8.8 MB (8794824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b96a5d219cafc293b68f995eea0528b3369efd25a46e311d24555ce8af1c1`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ce7da6f5dbee9cccee7a374cef703a1f6d58e7c6ceb44277befeb7b342f0ba7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dacadaa8e05016a6b0fa31f1eb111451d528b113d2048ba7506c60117c8f576`

```dockerfile
```

-	Layers:
	-	`sha256:41bb2cc6c12011a90b448e68cdab8cd47650effb3b281a708bb90450d2bd2045`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 6.4 MB (6429804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521730d2f4f9a7008aca3edcf3cbd555ea40389be2b67f105dfab454cc1cc16`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3d454b9bb282fc4b224560916df60eccaebb709ec5c12d51636cf2e0f0f269fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d72e237511d698382d62204c8899137f9dc69cbf0d44e74997414f8b3098`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19612df6c8b11eab84a5bb5b44627e00dda3eb5c29a447f494160d040a65be`  
		Last Modified: Fri, 14 Mar 2025 02:35:35 GMT  
		Size: 12.7 MB (12670786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e86b8a62be947487f7600d97973fd3bec39aa741065ac318f924584c42f4fa`  
		Last Modified: Fri, 14 Mar 2025 02:35:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd5ed02f9eea3f69b028908cc3bb42a7802cbfcb9e7c4b650706fd5e00eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 27.8 MB (27772449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d59bb902b97b58e0ca6f094a7cded9325884cdc29dd3cd8ec38cf7a5381eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1b487ac17f877a44f7dd3f30e241e0823150253e7a38f462acaf8ef2112c5`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98067ac8cbae75bbf2f044327990c759767da17c105c01cfb95c3374ee99e453`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14531b3ef2cef9e184f53e2b7e4e7c9e8248ca64ece49f4fd54af8a0f223d07f`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 5.6 MB (5601721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b906ba031f251bf0ef0a242f4e60886a554e681d095c997810f7435e91cf8`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 8.8 MB (8794808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c8576bf52489b87209e8f870c9359d00a83dbf0e12cdbbfe63c8553cb1d3`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:359a6d0257f11f723c53d31702f41c9b18f79212f4170a16c0a6c41bde36ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c7f595224b74c8817efa0a8c1b10c0f457dcce703e928cbe73604961603b3`

```dockerfile
```

-	Layers:
	-	`sha256:7f9e77adf90b5eb89666b262a468cb6059d123e31bd2659de464d7b6b6809161`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5334c6c7f7762ea59823ab0c8ff88b62b37a0760af0c6edc25aeb90d8d6c59`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.1`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.1` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.1-apache`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.30.1-fpm`

```console
$ docker pull backdrop@sha256:4be888f1c3dc7f12ec8127f2b999ee765f97cb4469b115cfb247e42598c286a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.30.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:b50428e2fd1b36cf43346258044e9c25be4fd62fd12244e95e493d4272e2fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187429753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650c622d5d1939636f59556367bb745ea4efcf0cb628481ce7ed47fc1b5c12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c13e0a380d1066144c01cfba2ab859d271383069f8c2b442f6141a93b518`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59086e1f0cf9b61be62079647cdc4eb36b89cea5edff168417222bb22b103614`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 104.3 MB (104329136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf44beef353412043b2b3904037068ca43282275644dc9b25bab39318df2e2f`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6f0658675ec128165643f91dc72a063ebc6ddff00c2fa1a0a30e21bceafa9`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 12.7 MB (12670866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c52b4d55386b4eb029ceb7084de7fd0755bb27068f7e5386d09191500cf532`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd31f0048a04f2deacdfa04e90000a90da078da75b8b711b6c82eef396b3934`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 27.8 MB (27828243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e79a7d807db4cf18efb8c69c13baefe71d1794e42bad07fa2f1d5d4e27b867`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789f3e28059cc460aa7b42e702b9031ae9a8be7a6c5f9a1cdef49b8fcfa5edbc`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79abfc0ffe8fae80874cefe1dc5a68e73f7d831fb061e7f0adc8e6c0729c376`  
		Last Modified: Mon, 17 Mar 2025 23:18:10 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a50659b9d6949bd73a7423e49d53e7615839c6090753685671927d4ad2737`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 5.6 MB (5588002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af74eb1ddb5c4f4102c3401b1979197f8c3ae0cbadbcfa3e7088be7257982`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 8.8 MB (8794824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b96a5d219cafc293b68f995eea0528b3369efd25a46e311d24555ce8af1c1`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ce7da6f5dbee9cccee7a374cef703a1f6d58e7c6ceb44277befeb7b342f0ba7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dacadaa8e05016a6b0fa31f1eb111451d528b113d2048ba7506c60117c8f576`

```dockerfile
```

-	Layers:
	-	`sha256:41bb2cc6c12011a90b448e68cdab8cd47650effb3b281a708bb90450d2bd2045`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 6.4 MB (6429804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521730d2f4f9a7008aca3edcf3cbd555ea40389be2b67f105dfab454cc1cc16`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.30.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3d454b9bb282fc4b224560916df60eccaebb709ec5c12d51636cf2e0f0f269fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d72e237511d698382d62204c8899137f9dc69cbf0d44e74997414f8b3098`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19612df6c8b11eab84a5bb5b44627e00dda3eb5c29a447f494160d040a65be`  
		Last Modified: Fri, 14 Mar 2025 02:35:35 GMT  
		Size: 12.7 MB (12670786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e86b8a62be947487f7600d97973fd3bec39aa741065ac318f924584c42f4fa`  
		Last Modified: Fri, 14 Mar 2025 02:35:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd5ed02f9eea3f69b028908cc3bb42a7802cbfcb9e7c4b650706fd5e00eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 27.8 MB (27772449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d59bb902b97b58e0ca6f094a7cded9325884cdc29dd3cd8ec38cf7a5381eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1b487ac17f877a44f7dd3f30e241e0823150253e7a38f462acaf8ef2112c5`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98067ac8cbae75bbf2f044327990c759767da17c105c01cfb95c3374ee99e453`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14531b3ef2cef9e184f53e2b7e4e7c9e8248ca64ece49f4fd54af8a0f223d07f`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 5.6 MB (5601721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b906ba031f251bf0ef0a242f4e60886a554e681d095c997810f7435e91cf8`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 8.8 MB (8794808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c8576bf52489b87209e8f870c9359d00a83dbf0e12cdbbfe63c8553cb1d3`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.30.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:359a6d0257f11f723c53d31702f41c9b18f79212f4170a16c0a6c41bde36ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c7f595224b74c8817efa0a8c1b10c0f457dcce703e928cbe73604961603b3`

```dockerfile
```

-	Layers:
	-	`sha256:7f9e77adf90b5eb89666b262a468cb6059d123e31bd2659de464d7b6b6809161`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5334c6c7f7762ea59823ab0c8ff88b62b37a0760af0c6edc25aeb90d8d6c59`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:4be888f1c3dc7f12ec8127f2b999ee765f97cb4469b115cfb247e42598c286a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:b50428e2fd1b36cf43346258044e9c25be4fd62fd12244e95e493d4272e2fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187429753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650c622d5d1939636f59556367bb745ea4efcf0cb628481ce7ed47fc1b5c12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c13e0a380d1066144c01cfba2ab859d271383069f8c2b442f6141a93b518`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59086e1f0cf9b61be62079647cdc4eb36b89cea5edff168417222bb22b103614`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 104.3 MB (104329136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf44beef353412043b2b3904037068ca43282275644dc9b25bab39318df2e2f`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6f0658675ec128165643f91dc72a063ebc6ddff00c2fa1a0a30e21bceafa9`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 12.7 MB (12670866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c52b4d55386b4eb029ceb7084de7fd0755bb27068f7e5386d09191500cf532`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd31f0048a04f2deacdfa04e90000a90da078da75b8b711b6c82eef396b3934`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 27.8 MB (27828243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e79a7d807db4cf18efb8c69c13baefe71d1794e42bad07fa2f1d5d4e27b867`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789f3e28059cc460aa7b42e702b9031ae9a8be7a6c5f9a1cdef49b8fcfa5edbc`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79abfc0ffe8fae80874cefe1dc5a68e73f7d831fb061e7f0adc8e6c0729c376`  
		Last Modified: Mon, 17 Mar 2025 23:18:10 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a50659b9d6949bd73a7423e49d53e7615839c6090753685671927d4ad2737`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 5.6 MB (5588002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af74eb1ddb5c4f4102c3401b1979197f8c3ae0cbadbcfa3e7088be7257982`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 8.8 MB (8794824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b96a5d219cafc293b68f995eea0528b3369efd25a46e311d24555ce8af1c1`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ce7da6f5dbee9cccee7a374cef703a1f6d58e7c6ceb44277befeb7b342f0ba7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dacadaa8e05016a6b0fa31f1eb111451d528b113d2048ba7506c60117c8f576`

```dockerfile
```

-	Layers:
	-	`sha256:41bb2cc6c12011a90b448e68cdab8cd47650effb3b281a708bb90450d2bd2045`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 6.4 MB (6429804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521730d2f4f9a7008aca3edcf3cbd555ea40389be2b67f105dfab454cc1cc16`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3d454b9bb282fc4b224560916df60eccaebb709ec5c12d51636cf2e0f0f269fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d72e237511d698382d62204c8899137f9dc69cbf0d44e74997414f8b3098`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19612df6c8b11eab84a5bb5b44627e00dda3eb5c29a447f494160d040a65be`  
		Last Modified: Fri, 14 Mar 2025 02:35:35 GMT  
		Size: 12.7 MB (12670786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e86b8a62be947487f7600d97973fd3bec39aa741065ac318f924584c42f4fa`  
		Last Modified: Fri, 14 Mar 2025 02:35:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd5ed02f9eea3f69b028908cc3bb42a7802cbfcb9e7c4b650706fd5e00eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 27.8 MB (27772449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d59bb902b97b58e0ca6f094a7cded9325884cdc29dd3cd8ec38cf7a5381eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1b487ac17f877a44f7dd3f30e241e0823150253e7a38f462acaf8ef2112c5`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98067ac8cbae75bbf2f044327990c759767da17c105c01cfb95c3374ee99e453`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14531b3ef2cef9e184f53e2b7e4e7c9e8248ca64ece49f4fd54af8a0f223d07f`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 5.6 MB (5601721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b906ba031f251bf0ef0a242f4e60886a554e681d095c997810f7435e91cf8`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 8.8 MB (8794808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c8576bf52489b87209e8f870c9359d00a83dbf0e12cdbbfe63c8553cb1d3`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:359a6d0257f11f723c53d31702f41c9b18f79212f4170a16c0a6c41bde36ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c7f595224b74c8817efa0a8c1b10c0f457dcce703e928cbe73604961603b3`

```dockerfile
```

-	Layers:
	-	`sha256:7f9e77adf90b5eb89666b262a468cb6059d123e31bd2659de464d7b6b6809161`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5334c6c7f7762ea59823ab0c8ff88b62b37a0760af0c6edc25aeb90d8d6c59`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:36b035cc540232f11c0138cc05055562f96c86dbec7815dae1020f326e053381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:a99348e3647566150fb02d822db0d515145dc960e4b1c20052f1c178a4b88140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191386134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b805de18b6368c8db6021d37afdd5883c3361a0a2a8595b269f686571e086de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44abce4cd77be4dd22299d1d4979cc6d32b860028fda868ff3480118e0478554`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07bcf613074c607e91776ff7ca66c50ad9e88c3b8783a1ef81a2e8267eb5da`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 5.6 MB (5581491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105f5fb382e46f44bc8457867570006df8e6121106c1f81fb97e498d986b3bb5`  
		Last Modified: Tue, 18 Mar 2025 00:17:22 GMT  
		Size: 8.8 MB (8794805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a592bae7fcccdca2f0fcddf8d6e0ef871bbec31c52342e732019779725c654d`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:f58d5ef828c3a7dbf155b5b12c6787df899bc5bea4feb976e7942acb555ab399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecddc1a22b6ded73c829f62e8dd82d24625c27d6882dc62abb5fb5b472b4eda`

```dockerfile
```

-	Layers:
	-	`sha256:2dd902b124d69e653d8828facf5f061df7a2c28182266bf7fd7efe2763355c04`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 6.9 MB (6940289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703febc08a2c890b6a97ec3addcee8a5f3660081deb85c6885dbc2219aa01785`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e83aad65ddbc3589e321f20be2895a2f007b7175c82520e576842b18a24af8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ce62c82250d9fb29bfcf4999f521f38001d21fe50218bc538945d761e8d2ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 07 Mar 2025 19:02:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 07 Mar 2025 19:02:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN a2enmod rewrite # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60277da4710b5dce71b782672f68e7ba09e600cd733d7bf510da5421b02789e1`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aa4cc1b0b6f0409778342f256b421aaa92845ef57a77665a01fa534c0e1b9`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 5.6 MB (5596886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f82bde1c3437880b5c1ba76443871e1b7489b6ce702bdc07fed33d0ba1df35`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 8.8 MB (8794814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596f18cedbec041ed634e0cbc1fff7ed49700afa4a3cb781ce869b97e2bb70d`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:714562d5f0052fea7cf1dc9fa2caa2fcc0d27ccb0cd56eb362e1b55f9c9f572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7851754fefde95944fbc8238c6dd074a843ccd0dac4c583851054026f97398`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ca7bed0c086eba4f1163fee725ed50486f47aa8f7e1cd87edc68bdb8e1406`  
		Last Modified: Fri, 14 Mar 2025 20:31:38 GMT  
		Size: 7.0 MB (6968753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704e3999f88dab5299036725623cde9951867f97464111658e4df6b305d82267`  
		Last Modified: Fri, 14 Mar 2025 20:31:37 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json
